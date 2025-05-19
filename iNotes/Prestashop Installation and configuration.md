1. Latest prestashop version download.  
    https://github.com/PrestaShop/PrestaShop/releases

2 . Installation Link and configuration. 
   https://www.atlantic.net/vps-hosting/how-to-install-prestashop-on-ubuntu-20-04/
   https://hostadvice.com/how-to/web-hosting/ubuntu/how-to-install-prestashop-on-ubuntu-18-04-server/
   https://linux.how2shout.com/how-to-install-prestashop-on-ubuntu-22-04-server/
   
3. Install latest prestashop version.
```
wget https://github.com/PrestaShop/PrestaShop/releases/download/8.2.0/prestashop_8.2.0.zip
```
- Unzip the the prestashop file
```
unzip prestashop_8.2.0.zip
```
4.  Create a Folder like `prestashop` in your `www/html/` apache2 server location, make sure your create folder in our user. 
```
cd /home/users/devendra.singh/www/html/
```
```
mkdir prestashop
```
 5. Unzip `prestashop.zip` file in `prestashop` directory.
```
unzip prestashop.zip -d /home/users/devendra.singh/www/html/prestashop/
```
6.  apache configuration.
```
vi /etc/apache2/sites-available/000-default.conf
```
 and add these lines.
```
<VirtualHost *:80>
         ServerAdmin admin@example.com
         DocumentRoot /home/users/devendra.singh/www/html/prestashop
         ServerName presta.com

         <Directory /home/users/devendra.singh/www/html/prestashop>
                Options +FollowSymlinks
                AllowOverride All
                Require all granted
         </Directory>

         ErrorLog ${APACHE_LOG_DIR}/example_error.log
         CustomLog ${APACHE_LOG_DIR}/example_access.log combined
</VirtualHost>
```
7. Host entry in our prestashop domain in local.
```
192.168.10.66     presta.com
```
8. Restart your apache2 service.
```
systemctl restart apache2
```
9. write url in search bar .
```
192.168.10.66/prestashop/
```