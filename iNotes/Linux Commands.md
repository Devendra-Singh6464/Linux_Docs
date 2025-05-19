If packages correctly not installed so.
```
sudo dpkg --configure -a
```

Node js (with out git-hub) install --
```bash
#!/bin/bash

#curl -sL [https://deb.nodesource.com/setup_22.x](https://deb.nodesource.com/setup_22.x) | sudo -E bash -  
curl -sL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt-get install nodejs -y
apt-get install nsolid -y 
nvm install 22
node -v
npm -v
```
-- Increase swap memory in ubuntu [allocated to memory]-------
```bash
sudo fallocate -l 10G /swapfile1
sudo chmod 600 /swapfile1
```
swapfile on.
```bash
sudo mkswap /swapfile1
sudo swapon /swapfile1
```
To check current swap usage:
```shell
swapon --show
```
permanent in-cress swap memory:	
```bash
echo '/swapfile1 none swap sw 0 0' | sudo tee -a /etc/fstab
```
Disable swap:
```shell
sudo swapoff <swap_file>
```
Permanently Disable Swap:
```shell
sudo vi /etc/fstab
```
** Comment out this line`# /swapfile1 none swap sw 0 0`
then
```shell
sudo swapoff -a
```
mount `hdd` to permanent.
```bash
/dev/sdb        /home/users/devendra.singh/hdd  ext4    defaults 0 0
/swapspace none swap sw 0 0

after this `reboot` system.
```
show the information about the `/dev/sdb` partition.
``` shell
fdisk -l /dev/sdb
```
check filesystem type.
``` shell
lsblk -f
```
if your file system type different so change to `ext4`.
``` shell
sudo umount /dev/sdb1
```
``` shell
sudo mkfs.ext4 /dev/sdb1
```
``` shell
mount -a
```
 Monitoring Setup:
```shell
sudo apt install glances
glances
```
check many users add a single groups.
``` shell
getent group <groupname>
```
where you store source code.
``` shell
/usr/src
```
No machine restart---
``` shell
/etc/NX/nxserver --restart
```
 Flush IP tables. 
``` shell
iptables -F
```
Check IP table allows status 
``` shell 
iptables -L
```

--- If you share a file 1 server to another server so using rsync 
Syntax =>
$ rsync -rav <folder(file)_name>/ <destination_username>:@destination_IP_address:<destination_address>
``` shell
rsync -rav devendra/ devendra.singh@192.168.15.138:/home/users/devendra.singh
```
-- create a new folder-
$ rsync -rav <folder(file)_name>/ <destination_username>:@destination_IP_address:<destination_address> <folder_name>

-- Using `scp` command copy and paste file to host server to remote server.
syntax--
``` shell
$ scp -r <folder_name> <destini_user_name>@<destini_ip>:<path where you copy folder>
```
``` shell
$ sudo usermod --shell /bin/sh devendra
```
If you want to change default shell a particular user
``` shell
chsh -s /bin/<shell_name> <user_name>
```
After check 
``` shell
grep <username> /etc/passwd
```
How to check how many shell download in my system
``` shell
echo $SHELLS
```
 and 
``` shell
cat /etc/shells
```
 How to check how to storage in my system
``` shell
du -sh (Specific_folder)
```
All data in my system
``` shell
df -hT
```
Check space in your disk.
``` shell
dh -h
```
- Check space in all files according to size.
``` shell
du -sh * | sort -h
```
Run this command to see all hidden files/folders and their sizes.
``` shell
du -sh .[!.]* * | sort -h
```
If you want to create a permanent alias so edit .bashrc file 
``` shell
vi .bashrc
```
edit--- 
``` shell
alias 32='ssh vagrant@192.168.1.32'
```
If you any change `.bashrc` file so run this command  
``` shell
source ~/.bashrc
```
If you want to check Kernel IP routing table.
``` shell
route -n
```
If you check all runing service port number 
``` shell
netstat -lntp
```
2. Create a Linux launcher icon.
``` shell
vi /usr/share/applications/<application_name.desktop>
```
How to check current default permission?
```shell
umask
```

chomd: change permission the file
chown: change user/owner permission
chgrp: change group permissioin
-- if you change the permission inside the folder all files so-------->
``` shell
chmod -R user:group <folder_name>
```
-- if you change 1 file permission so ------>
``` shell
chmod -r user:group <file_name> 
```
-- chown -c devendra 03-file 
``` shell
chgrp -c devendra 03-file
```
-- add use to another group--
``` shell
usermod -aG <group_name> <user_name>
```
acl commands
``` shell
getfacl 03-file 
```
 adding permission for user-
``` shell
setfacl -m u:user:rwx <file_name>
```
 adding permission for group-
``` shell
setfacl -m g:user:rwx <file_name>
```
 remove a sacific entry-
``` shell
setfacl -x u:user:rwx <file_name>
```
remove all entries-
``` shell
setfacl -b <file_name>
```
-- adding permission for user in all the files inside a folder
``` shell
setfacl -Rm "entry" <target_file/folder>
```
-- How to create to a user?
``` shell
useradd <usre_name>
adduser <user_name>
```
``` shell
useradd -g <group_name> -s /bin/bash -c "This is a tempory user" -m -d /home/<user_name> <user_name>
```

-- Modify user-----
root@wadmin-Veriton-M200-H310:/home# id alex
uid=1003(alex) gid=1003(alex) groups=1003(alex)

-- Change the default group 
root@wadmin-Veriton-M200-H310:/home# usermod -g demo alex

root@wadmin-Veriton-M200-H310:/home# id alex
uid=1003(alex) gid=1005(demo) groups=1005(demo)

root@wadmin-Veriton-M200-H310:~# usermod -g devendra dev
root@wadmin-Veriton-M200-H310:~# id dev
uid=1002(dev) gid=1001(devendra) groups=1001(devendra)

-- add new group but default group also there 
root@wadmin-Veriton-M200-H310:~# usermod -G demo dev

root@wadmin-Veriton-M200-H310:~# id dev
uid=1002(dev) gid=1001(devendra) groups=1001(devendra),1005(demo)
[]() 
change :-
```  shell
chage [-m mindays] [-M maxdays] [-d lastday] [-I inactive] [-E expiredate] [-W warndays] user_name
```

#### CONTROLLING SERVICE AND DAEMONS---
### systemd :
The systemd daemon manages startup for linux,including service start and service management in general.It actives system resources,server daemons and other processes both at boot time and on a runing system.

### Listin Service Units:
You use the systemctl command to exploer the currecnt state of the system.
This command without any arguments lists that are both loaded and active.
``` shell
systemctl
```
--This command lists only the service units with active activaton states.
``` shell
systemctl list-units --type=service
systemctl --type=service
```
Enabled : available across re-boot system.

1. if you want to set the limit any service to tack a memory so 
``` shell
systemctl set-property (service_name)httpd.service MemoryLimit=200M
```
``` shell
systemctl status httpd
```
oom kiiler: out of memory killer. 
if you restart the any service that means `pid` changed
how to cheack `pid`
``` shell
pidof <service_name>
```
if you reload the any servcie so service `pid` not changed-
``` shell
systemctl reload <service_name>
```
if you change apache default port:80 so
``` shell
vi /etc/httpd/conf/httpd.conf
```
and change the `listen`
``` shell
systemctl restart httpd
```
How to change host name:
``` shell
hostnamectl set-hostname <newname>
```
how check hdd check:
``` shell
lsblk
``` 

----Use the command to verify that the a service unit is currently active(running).-----
``` shell
systemctl is-active/enabled <servce_name>.service  
```
----To verify wheter the unit failed during startup.------
``` shell
systemctl is-failed <service_name>.service
```
--- how to check file system type-
``` shell
sudo blkid /dev/sda1
```

### Firewall d service on ubuntu------ 
how to start firewall d service on ubuntu
``` shell
systemctl start firewalld
```
enable--
``` shell
systemctl enable firewalld
```
 check status--
``` shell
systemctl status firewalld
```
stop the service-----
``` shell
systemctl stop <service_name>.service
```

`systemctl list-dependenies` this command displays a hierachy mapping of dependencies to start the service unit to list reverse dependencies(units that depend on the specified unit), use the --reverse opton with the command.
``` shell
systemctl list-dependencies <service_name>.service
```

### Masking and unmasking Services-----
Masking a Service: When you "mask" a service, you're essentially telling systemd to not start that service under any circumstances. It's a way to completely disable a service.

``` shell
systemctl mask <service_name>.service
```
``` shell
systemctl list unit-files --type==service
```
#### attempting to start a masked service unit fails.
--- how to unmask 
``` shell
systemctl umask <service_name>.service
```
Enabling Services to start or stop at Boot---
To start a service without root or password, use the systemctl enable command 
``` shell
systemctl enable <service_name>.service
``` 
 how many service given sudo privileges----
``` shell
vi /etc/sudoers
```
if using systemctl so. 
``` shell
%Wuser ALL = NOPASSWD: /usr/bin/systemctl
```
command-
``` shell
sudo systemctl start apache2
```

If you facing this type issue so ----
'
E: Failed to fetch https://packagecloud.io/AtomEditor/atom/any/dists/any/InRelease  402  Payment Required [IP: 52.9.110.75 443]
E: The repository 'https://packagecloud.io/AtomEditor/atom/any any InRelease' is no longer signed.
'
``` shell
vi /etc/apt/source.list
```
-- and commant the AtomEditor line
 If you check which all php version on your system and change the php version 
``` shell
update-alternatives --config php
```
Optional---
``` shell
update-alternatives --config php.phar
```
-- How to disable and enable service mode-----

 enmod service-
``` shell
a2enmod service
```
disable service
``` shell
a2dismod service
```
enable php version
``` shell
a2enmod php+version_name
```
disable php older version
``` shell
a2dismod php+version
```
check how many php service enabled
``` shell
ls /etc/apache2/mods-enabled/ | grep php
```

## File Transfer using SFTP
### Initiating an SFTP Connection
``` shell
sftp devendra@192.168.1.145
```
-- Transferring Files from Remote Servers to Local Systems.
> Syntax - get /path/to/remote/server/file.txt
``` shell
get /devendra/first_01
```
> You will see the file is getting copied into the local machine.
-- if you transfer folder so
``` shell
get -r devendra/
```

``` shell
mget /devendra/files_*.
```
> multiple files from remote server.

-- Transferring Files from Local Systems to Remote Servers
Syntax - put /path/to/local/file/abc.txt /path/to/remote/directory

``` shell
put /home/users/devendra.singh/help devendra/dev/
```
 
Extract tar file.
Syntax-
``` shell 
tar -xvzf  file_name
```
-- If Any package stops getting installed during installation
``` shell
apt-get install -f
```
-- Firefox update---
``` shell
apt install --only-upgrade firefox
```
-- If you check your hardware information
``` shell
apt install hardinfo
```
--- then
``` shell
hardinfo
```
-- Another option
``` shell
dmidecode
```
-- Check Your Windows 11 License Type
``` shell
slmgr.vbs /dli
```

#### The command will launch a Windows Script Host window. If it says RETAIL Channel, you can continue transferring the license to your new device. If it says OEM Channel, you cannot transfer the license.

-- Check 'groups/users' in linux-
``` shell
getent group/users  
```
 create a group-
``` shell
sudo addgroup 'group_name'
``` 
 Rename a group-
``` shell
sudo groupmod -n test demo1
```
 Add and remove users from a group
 how to check passwd in unencrypted form
``` shell
cat /etc/shadow
```
changing system date
``` shell
date
```
 (will display current date & time)
syntax--
``` shell
MMDDHHmmYYYY.ss
```
it will display no. of lines, words & characters in file.
``` shell
wc file1
```
if you facing system booting time issue and initramfs terminal is comming.
*Note: that's mean your file system issue*
``` shell
(initramfs) fsck /dev/sdaX -y
```
if you give sudo permission to a specific user. So add in the `/etc/sudoers` file.
Syntax.
<user_name> ALL = (ALL:ALL)  ALL
``` shell
devendra.singh ALL =(ALL:ALL) ALL
```
if you want to see error in any process so please go this directory. 
``` shell
cd /var/log/
```
if you watch continually apache error so - 
``` shell
tail -f /var/log/apache2/error.log
```
if you create alias in ubuntu so find alias and add what you want -
``` shell
vi .bashrc
```
after save '.barshrc' file
``` shell
source .bashrc
```
if your Google Chrome not open so-
``` shell
cd /home/users/<user_name>cd ./config/google-chrome
```
``` shell
ls
```
and  `SingletonLock` rename this file`SingletonLock.old`.

-- `shred` command is used to securely delete files from your system, making it much harder to recover them compared to standard deletion.
When you use `shred`, it overwrites the contents of a file multiple times with random data before deleting it. This makes it more difficult for anyone to recover the original data.
``` shell
shred -u <file_name>
```
- **`-u`**: This option tells `shred` to **unlink** (delete) the file after shredding it.
- **`-n 3`**: This specifies the number of times to overwrite the file (default is 3(default) times).

The shred command is also used to overwrite the data of a drive. Drive contains a huge amount of data, hence, a lot of time will be required to shred this data.
syntax:
``` shell
shred <file_name>
```
example.
``` shell
shred /dev/sda1
```
If you only intercept your data not delete so 
``` shell
shred <file_name>
```
how to check how many bit in my system
``` shell
getconf LONG_BIT
```
if set default editor.
``` shell
update-alternatives --config editor
```
Allow users to change PHP version without sudo in ubuntu.
``` shell
devendra.singh ALL=(ALL) NOPASSWD: /usr/bin/update-alternatives --config php
```
if you want to check packages alternatives so 
``` shell
devendra.singh ALL=(ALL) NOPASSWD: /usr/bin/update-alternatives 
```
Check Kernel Logs: Sometimes more information about the error can be found in the kernel logs. Use:
``` shell 
dmesg | tail
```
Retrieve the inode of a file.
``` shell
ls -i filename
```
example commands to add new disk
``` shell
lsblk                     # list all disks and partitions
sudo fdisk /dev/sdb       # let's suppose new disk is /dev/sdb
sudo mkfs.ext4 /dev/sdb1  # make filesystem(e.g., ext4) on partition 1
sudo mount /dev/sdb1 /mnt # mount new filesystem to /mnt directory
```
The following are common commands to manage disks:

- Use `lsblk` to list all block devices (disk and partitions).
- Use `fdisk /dev/sdX` to create a new partition on a disk.
- Use `mkfs.ext4 /dev/sdX1` to create a new filesystem on a partition.
- Use `mount /dev/sdX1 /mount/point` to mount a filesystem to a directory.

- If you are facing this type of problem then user cannot save or create his file.
```error
W: Problem unlinking the file /var/cache/apt/pkgcache.bin - RemoveCaches (30: Read-only file system)
W: Problem unlinking the file /var/cache/apt/srcpkgcache.bin - RemoveCaches (30: Read-only file system)
```
So `restart` your system and `initramfs` terminal frount of your 
top of terminal you see `/dev/<type>` that means your system no  permission this file. so run this command 
``` shell 
fsck /dev/sda<type> -y
```
``` shell 
exit
```

--- kazam simplescreenrecord Recording the Black Screen in linux.
Open the file.
``` shell
vi /etc/gdm3/custom.conf
```
 and uncomment this line. 
` #WaylandEnable=false `
To 
` WaylandEnable=false `

If You check how many ports run on.
``` shell
Starting Nmap 7.80 ( https://nmap.org ) at 2024-10-09 09:24 IST
Nmap scan report for _gateway (192.168.15.1)
Host is up (0.00048s latency).

``` 
-- If you redirect output in a file (saving output to a file):
syntax.
``` shell
command > file.txt
```
example.
``` shell
ls > file.txt
```
-- If you want to capture both standard output and standard error in the same file, use:
``` shell
command > output.txt 2>&1
```
if you know the any topic related to linux command definition in 1 line. 
``` shell
whatis route
```
error
``` shell
route: nothing appropriate.
```
run : update manual entry's.
``` shell
mandb
```
If you block to single IP `ssh` on your system.
``` shell
vi /etc/hosts.deny
```
-- syntax:
`sshd: <system_ip>` 
``` shell
sshd: 192.168.1.32
```
Change Default `SSH` Port.
``` shell
vi /etc/ssh/sshd_config
```
uncomment this and change port.
``` shell
#Port 22
```
- Outgoing ssh connection port change.
``` shell 
vi /etc/ssh/ssh_config
```
- Incomming ssh port change.
``` shell 
vi /etc/ssh/sshd_config
```
-- Check any service process ID.
``` shell
pgrep <service_name>
```
if you kill process 
``` shell
pgrep <service_name> | xargs kill -9
```
if see parent process and child process.
``` shell
pstree
```
-- show all run process for user.
``` shell
pstree -p -u devendra.singh
```
how to forward process to background.
syntax.
``` shell
<cammand> &
```
	
``` shell
sleep 20 &
```
--- If you `erase` your disk fully no any one can access after erase data using any data recovery tool so.
syntax.
`badblocks -ws <disk_path>`
``` shell
badblocks -ws /dev/sda
```
&&
syntax.
`dd =if/dev/zero of=/dev/<disk_name>`
``` shell
dd if=/dev/zero of=/dev/sda
```

 1. The `shred` command overwrites the contents of a file multiple times, making recovery difficult. By default, it overwrites the file three times, but you can specify the number of overwrites with the `-n` option.
``` shell
shred -n 5 -z -u filename
```
2. `wipe`
``` shell
wipe filename 
```
after add `scsi` disk  and scan without reboot system.
``` shell
ls /sys/class/scsi_host/ | while read host ; do echo "- - -" > /sys/class/scsi_host/$host/scan ; done
```
If you check graphically.
``` shell
for x in `ls /sys/class/scsi_host/` ; do echo " $x scanned"; > /sys/class/scsi_host/$x/scan ; done
```
check your disk type.
syntax.
``` shell
sudo parted /dev/sdX print
```
``` shell
parted /dev/sdb print
```
-- check all LDAP users:
``` shell
getent passwd
```
ubuntu drivers install.
``` shell
sudo ubuntu-drivers autoinstall
```
``` shell
sudo systemctl status wpa_supplicant
```
use `sed` command [if you add some changes in the file or script so use set command].
``` shell
sed -i 's/devendra/deepak/g' 01.sh 
```
`this command changed devendra to deepak in 01.sh file`.


sudo rm -rf /var/lib/apt/lists/*
sudo rm -rf /var/lib/command-not-found/*

sudo vi /etc/apt/apt.conf.d/50command-not-found
and comment this line
``` shell
#APT::Update::Post-Invoke-Success
```
``` shell
sudo apt --fix-broken install
```

Download the Elasticsearch Debian Package. 
``` shell
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.15.0-amd64.deb
```

Check all services and which they are port runing .
``` shell
sudo lsof -i -P -n | grep LISTEN
```

how to update composer.
install composer.
```shell
sudo apt install composer
```

``` shell
composer self-update
```
  Use return the back version
``` shell
composer self-update --rollback
```

how to check redis extension enabled or not.
``` shell
php --ini | grep redis
```
- disable php version.
``` shell
vi /etc/php/7.4/mods-available/<extensions>
```
and 
``` shell
; configuration for php common module
; priority=20
extension=fileinfo.so
```
`;` : comment the extension.
``` shell
; configuration for php common module
; priority=20
; extension=fileinfo.so
```
dismod extensions.
``` shell
phpdismod <extension>
```
restart your web server
``` shell
systemctl restart apache2
```
Run to see a list of processes and their ports.
``` shell
sudo netstat -tlpn 
```
- which server runing domain.
``` shell
dig mx <domain_name>
```

- check all php extensions.
``` shell
php -m
```
- Specific versions
``` shell
php8.1 -m
```

If you want to create a tar file.  

*syntax*
```shell
tar -cvf <file_name> <path/to/which file you want to take backup>
```
``` shell
tar -cvf notes_backup.tar /home/users/devendra.singh/myDocs
```


*How do I fix GNU GRUB 2.04?*
* Set the correct partition
``` shell
set root=(hd0,gpt2)     # Replace with your partition
set prefix=(hd0,gpt2)/boot/grub
insmod normal
normal
```

* If it boots, **reinstall GRUB permanently**
``` shell 
sudo grub-install /dev/sda
sudo update-grub
reboot
```

To allow change of wifi-connection without admin password create new file

``` shell
sudo vi /etc/polkit-1/localauthority/50-local.d/org.freedesktop.NetworkManager.pkla
```

with the following content:

``` shell
[Enable NetworkManager]
Identity=unix-group:netdev
Action=org.freedesktop.NetworkManager.*
ResultAny=no
ResultInactive=no
ResultActive=yes
```

```shell
#!/bin/bash
touch /etc/polkit-1/localauthority/50-local.d/10-network-manager.pkla
cat > /etc/polkit-1/localauthority/50-local.d/10-network-manager.pkla <<EOL
[Let all users modify system settings for network]
Identity=unix-user:*
Action=org.freedesktop.NetworkManager.settings.modify.system
ResultAny=yes
ResultInactive=yes
ResultActive=yes
EOL

```

Remove permission to stander user delete files.
*Go this location and change*
``` shell
vim /usr/share/X11/xkb/symbols/pc
```

```shell
hidden partial alphanumeric_keys
xkb_symbols "editing" {
    key <PRSC> {
        type= "PC_ALT_LEVEL2",
        symbols[Group1]= [ Print, Sys_Req ]
    };
    key <SCLK> {        [  Scroll_Lock          ]       };
    key <PAUS> {
        type= "PC_CONTROL_LEVEL2",
        symbols[Group1]= [ Pause, Break ]
    };
    key  <INS> {        [  Insert               ]       };
    key <HOME> {        [  Home                 ]       };
    key <PGUP> {        [  Prior                ]       };
    key <DELE> {        [  Delete               ]       };
    key  <END> {        [  End                  ]       };
    key <PGDN> {        [  Next                 ]       };

    key   <UP> {        [  Up                   ]       };
    key <LEFT> {        [  Left                 ]       };
    key <DOWN> {        [  Down                 ]       };
    key <RGHT> {        [  Right                ]       };
};
                                                                    
```

* After change *
```shell
hidden partial alphanumeric_keys
xkb_symbols "editing" {
    key <PRSC> {
        type= "PC_ALT_LEVEL2",
        symbols[Group1]= [ Print, Sys_Req ]
    };
    key <SCLK> {        [  Scroll_Lock          ]       };
    key <PAUS> {
        type= "PC_CONTROL_LEVEL2",
        symbols[Group1]= [ Pause, Break ]
    };
    key  <INS> {        [  Insert               ]       };
    key <HOME> {        [  Home                 ]       };
    key <PGUP> {        [  Prior                ]       };
    key <DELE> {        [  NoSymbol             ]       };
    key  <END> {        [  End                  ]       };
    key <PGDN> {        [  Next                 ]       };

    key   <UP> {        [  Up                   ]       };
    key <LEFT> {        [  Left                 ]       };
    key <DOWN> {        [  Down                 ]       };
    key <RGHT> {        [  Right                ]       };
};

```

After that add this file to .bashrc file
```shell
vi .bashrc
```

```shell
rm() {  
:  
}  
rmdir() {  
:  
}
```

```shell
source .bashrc
```

* If some time your localhost not working and apache2 service working fine so   rename this file `.htaccess` this file in `/home/users/devendra.singh/www/` this directory.
