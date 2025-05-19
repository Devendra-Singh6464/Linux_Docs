
Go to
C:  `xampp\htdocs`

edit file-
`apache/conf/httpd.conf` file
```php
DocumentRoot "C:/xampp/htdocs"
<Directory "C:/xampp/htdocs">
```

and edit `C:/<your_path>` If you want so outher wise `htdocs` folder under files remove ti.
```php
DocumentRoot "C:/xampp/devenra.singh"
<Directory "C:/xampp/devendra.singh">
```
and then restart the apache.