# Mkcert is a simple tool for making locally-trusted development certificates.

Once all the packages are installed, download the latest version of Mkcert from Github.
``` shell 
wget https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64
```
After downloading Mkcert, move the downloaded binary to the system path
``` shell
mv mkcert-v1.4.3-linux-amd64 /usr/bin/mkcert
```
Next, set the execution permission to the mkcert:
``` shell
chmod +x /usr/bin/mkcert
```
install libnss3-tools:
``` shell
apt install libnss3-tools
```
check mkcert version:
``` shell
mkcert --version
```
switch your local user and generate a local CA certificate:
``` shell
mkcert -install
```
Generate a Certificate for Local Website:
``` shell
mkcert deepaktxt.com "*.deepaktxt.com" deepaktxt.test localhost 127.0.0.1 ::1
```
After this [optional]: -
``` shell
mkcert -key-file deepaktxtkey.pem -cert-file deepaktxtcert.pem deepaktxt.com *.deepaktxt.com
```
go to root: 
``` shell
mv deepaktxtcert.pem /etc/ssl/certs/
```
``` shell
mv deepaktxtkey.pem /etc/ssl/private/
```
Edit this line:-
``` shell
vi /etc/apache2/sites-available/default-ssl.conf
```

``` shell
SSLCertificateFile      /etc/ssl/certs/deepaktxtcert.pem
SSLCertificateKeyFile /etc/ssl/private/deepaktxtkey.pem
```
*NOTE: domain body items  add in `default-ssl.conf` * .
``` shell
ServerName saas-modules.com
ServerAlias site1.saas-modules.com
ServerAlias site2.saas-modules.com
ServerAlias site3.saas-modules.com
ServerAlias site4.saas-modules.com

ServerAdmin webmaster@localhost
DocumentRoot /home/users/mukul.sharma/www/html/modules/saas-modules/public
```
                
``` shell
sudo a2enmod ssl
```
``` shell
sudo a2enmod headers
```
``` shell
sudo a2ensite default-ssl
```

Try:
```
wget [https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64](https://github.com/FiloSottile/mkcert/releases/download/v1.4.3/mkcert-v1.4.3-linux-amd64)  
mv mkcert-v1.4.3-linux-amd64 /usr/bin/mkcert  
chmod +x /usr/bin/mkcert  
apt install libnss3-tools  
su username  
mkcert -install  
mkcert abhisheklocal.com "*.abhisheklocal.com" abhisheklocal.test localhost 127.0.0.1 ::1  
  
mkcert -key-file abhishekkey.pem -cert-file abhishekcert.pem abhisheklocal.com *.abhisheklocal.com  
  
mv abhishekcert.pem /etc/ssl/certs/  
mv abhishekkey.pem /etc/ssl/private/  
vim /etc/apache2/sites-available/default-ssl.conf  
sudo a2enmod ssl  
sudo a2enmod headers  
sudo a2ensite default-ssl
```




Demo try:
--------
devendra.singh@devendra138:~$ mkcert -install
Created a new local CA 💥
Sudo password:
Sorry, try again.
Sudo password:
Sorry, try again.
Sudo password:

[1]+  Stopped  	               mkcert -install
devendra.singh@devendra138:~$ mkcert -install
Sudo password:

[2]+  Stopped                 mkcert -install
devendra.singh@devendra138:~$ mkcert -install
Sudo password:

[3]+  Stopped                 mkcert -install
devendra.singh@devendra138:~$ exit
exit
There are stopped jobs.
devendra.singh@devendra138:~$ exit
exit
Sudo password:
root@devendra138:~# Sudo password:
Sudo password:

root@devendra138:~# 
root@devendra138:~# vi /etc/sudoers
root@devendra138:~# su devendra.singh
devendra.singh@devendra138:/root$ cd
devendra.singh@devendra138:~$ mkcert -install
Sudo password:
Sorry, try again.
Sudo password:
The local CA is now installed in the system trust store! ⚡️
The local CA is now installed in the Firefox and/or Chrome/Chromium trust store (requires browser restart)! 🦊
The local CA is already installed in Java's trust store! 👍

devendra.singh@devendra138:~$ exit
exit
root@devendra138:~# vi /etc/sudoers
root@devendra138:~# su devendra.singh
devendra.singh@devendra138:/root$ cd
devendra.singh@devendra138:~$ mkcert bhandari.demo "*.bhandari.demo" bhandari.test localhost 127.0.0.1 ::1

Created a new certificate valid for the following names 📜
 - "bhandari.demo"
 - "*.bhandari.demo"
 - "bhandari.test"
 - "localhost"
 - "127.0.0.1"
 - "::1"

Reminder: X.509 wildcards only go one level deep, so this won't match a.b.bhandari.demo ℹ️

The certificate is at "./bhandari.demo+5.pem" and the key at "./bhandari.demo+5-key.pem" ✅

It will expire on 26 November 2026 🗓

devendra.singh@devendra138:~$ mkcert -key-file bhandarikey.pem -cert-file bhandaricert.pem bhandari.demo *.bhandari.demo

Created a new certificate valid for the following names 📜
 - "bhandari.demo"
 - "*.bhandari.demo"

Reminder: X.509 wildcards only go one level deep, so this won't match a.b.bhandari.demo ℹ️

The certificate is at "bhandaricert.pem" and the key at "bhandarikey.pem" ✅

It will expire on 26 November 2026 🗓

devendra.singh@devendra138:~$ exit
exit
root@devendra138:~# cd /home/users/devendra.singh/
root@devendra138:/home/users/devendra.singh# ls
 abcd			   dev.txt		    mycode		  start_script_run
 after_SSD_changed	   Documents		    mycodefile		  start.sh
 attachment_block	   Downloads		    mysql_data_bkp.md	  task
 bhandaricert.pem	   eclipse		    myvm		  tasks
 bhandari.demo+5-key.pem   eclipse-workspace	    note		  Templates
 bhandari.demo+5.pem	   f1.py		    Note		  test
 bhandarikey.pem	   flutter		    notes		 'Untitled Document 1'
 bkp.sql		   gocode		    opencart_install.md   update_npm
 bkup.gz		   hdd			    paswd		  Videos
 core			   hed.txt		    php_installation	 'VirtualBox VMs'
 cron			   keyboard_list	    Pictures		  wget-log
 cron.txt		  'left employee massage'   Public		  windows_laptop
 Desktop		   linux_admin_cmd	    replys		  www
 desktop_script		   Linux.pdf		    service_check
 devendra		   Music		    snap
root@devendra138:/home/users/devendra.singh# vi b
bhandaricert.pem         bhandari.demo+5.pem      bkp.sql
bhandari.demo+5-key.pem  bhandarikey.pem          bkup.gz
root@devendra138:/home/users/devendra.singh# vi b
bhandaricert.pem         bhandari.demo+5.pem      bkp.sql
bhandari.demo+5-key.pem  bhandarikey.pem          bkup.gz
root@devendra138:/home/users/devendra.singh# mv bhandaricert.pem /etc/ss
ssh/ ssl/ 
root@devendra138:/home/users/devendra.singh# mv bhandaricert.pem /etc/ssl/certs/
root@devendra138:/home/users/devendra.singh# mv bhandarikey.pem /etc/ss
ssh/ ssl/ 
root@devendra138:/home/users/devendra.singh# mv bhandarikey.pem /etc/ssl/private/
root@devendra138:/home/users/devendra.singh# vi /etc/apache2/sites-available/default-ssl.conf 
root@devendra138:/home/users/devendra.singh# cd /etc/ssl/private/
root@devendra138:/etc/ssl/private# ls
apache-selfsigned.key  bhandarikey.pem	ssl-cert-snakeoil.key
root@devendra138:/etc/ssl/private# sudo a2enmod ssl
Considering dependency setenvif for ssl:
Module setenvif already enabled
Considering dependency mime for ssl:
Module mime already enabled
Considering dependency socache_shmcb for ssl:
Module socache_shmcb already enabled
Module ssl already enabled
root@devendra138:/etc/ssl/private# sudo a2enmod headers
Module headers already enabled
root@devendra138:/etc/ssl/private# sudo a2ensite default-ssl
Site default-ssl already enabled
root@devendra138:/etc/ssl/private# service apache2 restart
root@devendra138:/etc/ssl/private# 
