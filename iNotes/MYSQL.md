* MySQL completely remove from the Ubuntu *
``` shell 
systemctl disable mysql
```
```shell
sudo killall -9 mysqld
```
```shell
sudo killall -9 mysql
```
```shell
sudo apt-get remove --purge mysql-\*
```
```shell
apt-get remove --purge mysql*
```
```shell
apt-get purge mysql*
```
```shell
apt-get autoremove
```
```shell
apt-get autoclean
```
``` shell
whereis mysql
```
``` shell
cd /etc/
rm -rf mysql
```

* Install MYSQL in Ubuntu *
``` shell
sudo apt install mysql-server
```
Mysql services
``` shell
systemctl status mysql.service
```
``` shell
systemctl stop mysql.service
```
``` shell
systemctl restart mysql.service
```
- Mysql root user login security script.
``` shell
sudo mysql_secure_installation
```
*note- demo*
```
root@wadmin34:~# sudo mysql_secure_installation

Securing the MySQL server deployment.

Enter password for user root: 

VALIDATE PASSWORD COMPONENT can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD component?

Press y|Y for Yes, any other key for No: n
Using existing password for root.
Change the password for root ? ((Press y|Y for Yes, any other key for No) : n

 ... skipping.
By default, a MySQL installation has an anonymous user,
allowing anyone to log into MySQL without having to have
a user account created for them. This is intended only for
testing, and to make the installation go a bit smoother.
You should remove them before moving into a production
environment.

Remove anonymous users? (Press y|Y for Yes, any other key for No) : n

 ... skipping.


Normally, root should only be allowed to connect from
'localhost'. This ensures that someone cannot guess at
the root password from the network.

Disallow root login remotely? (Press y|Y for Yes, any other key for No) : n

 ... skipping.
By default, MySQL comes with a database named 'test' that
anyone can access. This is also intended only for testing,
and should be removed before moving into a production
environment.


Remove test database and access to it? (Press y|Y for Yes, any other key for No) : n

 ... skipping.
Reloading the privilege tables will ensure that all changes
made so far will take effect immediately.

Reload privilege tables now? (Press y|Y for Yes, any other key for No) : n

 ... skipping.
All done! 
root@wadmin34:~# 
```
- Open the MySQL Prompt: 
``` shell
sudo mysql
```
 - Set mysql `root` user password.111
``` shell 
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'webkul';
```
- `Error`:               
`ERROR 1819 (HY000): Your password does not satisfy the current policy requirements`
- Change the Password policy.
``` shell
SET GLOBAL validate_password.policy = LOW;
```
``` shell
SET GLOBAL validate_password.length = 6;
```
```
FLUSH PRIVILEGES;
```
