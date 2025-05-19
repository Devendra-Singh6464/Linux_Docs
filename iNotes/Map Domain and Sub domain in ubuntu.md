Go to root  
``` shell
vi /etc/hosts
```

and add this line
``` shell
127.0.0.1    <domain_name>
127.0.0.1    <subdomain_name>
```

go to this `vi /etc/apache2/sites-available/000-default.conf`   directory and add this line

``` shell
<VirtualHost *:80>
       
        ServerName bhandari.demo
        ServerAlias dev.bhandari.demo

        ServerAdmin webmaster@localhost
        DocumentRoot /home/users/devendra.singh/www/html

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined

        # Redirect "/" "https://127.0.0.1"
</VirtualHost>
```

write ServerName (domain_name)
write  ServerAlias(subdomain_name)
DocumentRoot <your_path>

last ensite the changed file
`````` shell
a2ensite 000-default.conf
```
