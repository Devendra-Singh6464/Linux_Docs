``` shell 
   
vim /etc/mysql/my.cnf  
[client]  
default-character-set=utf8  
  
[mysql]  
default-character-set=utf8  
  
[mysqld]  
collation-server = utf8_unicode_ci  
character-set-server = utf8  
default-authentication-plugin=mysql_native_password  
  
service mysql restart
``` 
