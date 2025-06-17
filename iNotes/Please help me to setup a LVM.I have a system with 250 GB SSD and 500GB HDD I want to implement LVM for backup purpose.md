## **📌 Step-by-Step LVM Setup for Backup**

We will:

1. **Initialize both disks as Physical Volumes (PVs).**
    
2. **Combine them into a Volume Group (VG).**
    
3. **Create Logical Volumes (LVs) for storage & backups.**
    
4. **Mount them for use.**
    

---

### **🔹 Step 1: Check Available Disks**

First, identify your disks:
``` shell
lsblk   # List all disks and partitions
```

Example output:
```shell
NAME        MAJ:MIN RM   SIZE RO TYPE MOUNTPOINT
sda           8:0    0 232.9G  0 disk   # SSD (250GB)
├─sda1        8:1    0   512M  0 part  /boot/efi
└─sda2        8:2    0 232.4G  0 part  /
sdb           8:16   0 465.8G  0 disk   # HDD (500GB)
```


**Note:**

- `sda` = SSD (likely your OS disk)
    
- `sdb` = HDD (500GB, unused)
    
⚠️ **Warning:**

- **Do not modify `sda` if it contains your OS!**
    
- We will use **`sdb` (HDD)** for LVM.

### **Step 2: Create a Physical Volume (PV)**

Initialize the HDD (`sdb`) as an LVM Physical Volume:

```shell
sudo pvcreate /dev/sdb   # Initialize HDD for LVM
```

Verify:
```shell
sudo pvs   # List Physical Volumes
```

Output should show:
```shell
PV         VG  Fmt  Attr PSize   PFree  
/dev/sdb       lvm2 ---  465.76g 465.76g
```

### **Step 3: Create a Volume Group (VG)**

Create a VG named `backup_vg` using the HDD:
```shell
sudo vgcreate backup_vg /dev/sdb
```

Verify:
```shell
sudo vgs   # List Volume Groups
```

Output:
```shell
VG        #PV #LV #SN Attr   VSize   VFree  
backup_vg   1   0   0 wz--n- 465.76g 465.76g
```

### **Step 4: Create Logical Volumes (LVs)**

Now, create LVs inside `backup_vg` for different purposes.

#### **Option 1: Single Backup LV (Recommended for Simplicity)**

```shell
sudo lvcreate -n backup_lv -L 400G backup_vg   # Reserve ~400GB for backups
```

_(Leaves some free space for snapshots or expansion.)_
1. **`sudo`** → "I need admin rights to do this!"
2. **`lvcreate`** → "Hey LVM, **create a new storage drawer**!"
3. **`-n backup_lv`** → "Name this drawer **`backups`** (so I can find it later)."
4. **`-L 400G`** → "Make it **400GB big**."
5. **`backup_vg`** → "Put this drawer inside the **`my_storage`** pool (Volume Group)."

#### **Option 2: Multiple LVs (For Organized Backups)**
```shell
sudo lvcreate -n docs_lv -L 200G backup_vg   # For documents
sudo lvcreate -n media_lv -L 200G backup_vg   # For photos/videos
```

Verify:
```shell
sudo lvs   # List Logical Volumes
```

Output:
```shell
LV        VG        Attr       LSize   Pool Origin Data%  
backup_lv backup_vg -wi-a----- 400.00g
```

### **Step 5: Format & Mount the LV**

#### **1. Format as ext4 (recommended for Linux backups)**
```shell
sudo mkfs.ext4 /dev/backup_vg/backup_lv
```

#### **2. Create a Mount Point**
```shell
sudo mkdir /mnt/backup   # Create a directory for mounting
```

#### **3. Mount the LV**
```shell
sudo mount /dev/backup_vg/backup_lv /mnt/backup
```

#### **4. Auto-Mount on Boot**

Edit `/etc/fstab`:
```shell
sudo nano /etc/fstab
```

Add this line:
```shell
/dev/backup_vg/backup_lv  /mnt/backup  ext4  defaults  0  2
```

Save (`Ctrl+O`, `Enter`, `Ctrl+X`).

Verify mounting:
```shell
sudo mount -a   # Reload fstab
df -h /mnt/backup   # Check if mounted
```

## **Step 6: Using LVM for Backups**

Now, you can use `/mnt/backup` to store your backups.

### **Example Backup Commands**

1. **Copy files manually:**
```shell
cp -r ~/Documents /mnt/backup/
```

2. **Use `rsync` for incremental backups:**
```shell
rsync -avz ~/Pictures /mnt/backup/
```

3. **Schedule automated backups with `cron`.**

## **Expanding LVM in the Future**

If you later add **another HDD (e.g., 1TB)**, you can:

1. **Add it to `backup_vg`:**
```shell
sudo pvcreate /dev/sdc   # New disk
sudo vgextend backup_vg /dev/sdc
```

2. **Expand `backup_lv`:**
```shell
sudo lvextend -L +500G /dev/backup_vg/backup_lv
sudo resize2fs /dev/backup_vg/backup_lv   # Resize filesystem
```

## **📌 Summary**

✅ **`sdb (HDD)` → PV → VG (`backup_vg`) → LV (`backup_lv`)**  
✅ **Formatted as ext4 and mounted at `/mnt/backup`**  
✅ **Ready for storing backups!**
