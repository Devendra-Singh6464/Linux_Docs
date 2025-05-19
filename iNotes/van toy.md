## Multi iso bootable pandrive ----
 
1. Install vantoy tar file 
```
https://ventoy.net/en/download.html
```
2. After install tar file untar the file. 
```
tar -xf filename.tar
```
1. Go this ​directory---
```
ventoy-1.0.99
```
2. Run script
```
./Ventoy2Disk.sh
```
3. Then cleck USB mount location
```
lsblk
```
4. Your USB mount location here-
```
syntax-- /media/<user_name>/
/media/devendra.singh/
```
5. Then run this command -
Sysntax-
/Ventoy2Disk.sh -i /dev/file_name
```
/Ventoy2Disk.sh -i /dev/sdd
```
6. After this script run you got error-
```
Error: Failed to access /dev/sdc, maybe root privilege is needed!
```
7. After Go to root and run again this command-----  
```
/Ventoy2Disk.sh -i /dev/sdd
```
8. If you got this error `/dev/sdd is already mounted, please umount it first!`
----please unmount /dev/sdd
```
umount /dev/sdd
```
