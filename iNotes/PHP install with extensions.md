``` shell 
If you want to change your PHP version, please follow these commands.

1. Change the PHP version and select the version you want.  
sudo update-alternatives --config php

2. Disable php version  
sudo a2dismod <your_enable_php_version>

3. Enable php version  
sudo a2enmod <your_php_version>

Before enabling any PHP version, make sure to disable the older PHP version.

1. Restart your apache.
sudo /etc/init.d/apache2 restart
```

sudo add-apt-repository ppa:ondrej/php
sudo apt-get update
``` shell 

apt-get -y install php5.6 php5.6-curl php5.6-intl php5.6-gd php5.6-dom php5.6-mcrypt php5.6-iconv php5.6-xsl php5.6-mbstring php5.6-ctype php5.6-zip php5.6-pdo php5.6-xml php5.6-bz2 php5.6-calendar php5.6-exif php5.6-fileinfo php5.6-json php5.6-mysqli php5.6-mysql php5.6-posix php5.6-tokenizer php5.6-xmlwriter php5.6-xmlreader php5.6-phar php5.6-soap php5.6-mysql php5.6-fpm libapache2-mod-php5.6 php5.6-gmp php5.6-bcmath php5.6-apcu php5.6-redis php5.6-imagick php5.6-imap php5.6-xdebug

```

&&
```

apt-get -y install php7.0 php7.0-curl php7.0-intl php7.0-gd php7.0-dom php7.0-mcrypt php7.0-iconv php7.0-xsl php7.0-mbstring php7.0-ctype php7.0-zip php7.0-pdo php7.0-xml php7.0-bz2 php7.0-calendar php7.0-exif php7.0-fileinfo php7.0-json php7.0-mysqli php7.0-mysql php7.0-posix php7.0-tokenizer php7.0-xmlwriter php7.0-xmlreader php7.0-phar php7.0-soap php7.0-mysql php7.0-fpm libapache2-mod-php7.0 php7.0-gmp php7.0-bcmath php7.0-apcu php7.0-redis php7.0-imagick php7.0-imap php7.0-xdebug

```

&&
```
apt-get -y install php7.1 php7.1-curl php7.1-intl php7.1-gd php7.1-dom php7.1-mcrypt php7.1-iconv php7.1-xsl php7.1-mbstring php7.1-ctype php7.1-zip php7.1-pdo php7.1-xml php7.1-bz2 php7.1-calendar php7.1-exif php7.1-fileinfo php7.1-json php7.1-mysqli php7.1-mysql php7.1-posix php7.1-tokenizer php7.1-xmlwriter php7.1-xmlreader php7.1-phar php7.1-soap php7.1-mysql php7.1-fpm libapache2-mod-php7.1 php7.1-gmp php7.1-bcmath php7.1-apcu php7.1-redis php7.1-imagick php7.1-imap php7.1-xdebug

```

&&
```
apt-get -y install php7.2 php7.2-curl php7.2-intl php7.2-gd php7.2-dom php7.2-iconv php7.2-xsl php7.2-mbstring php7.2-ctype php7.2-zip php7.2-pdo php7.2-xml php7.2-bz2 php7.2-calendar php7.2-exif php7.2-fileinfo php7.2-json php7.2-mysqli php7.2-mysql php7.2-posix php7.2-tokenizer php7.2-xmlwriter php7.2-xmlreader php7.2-phar php7.2-soap php7.2-mysql php7.2-fpm libapache2-mod-php7.2 php7.2-gmp php7.2-bcmath php7.2-apcu php7.2-redis php7.2-imagick php7.2-imap php7.2-xdebug

```

&&     
```

apt-get -y install php7.3 php7.3-curl php7.3-intl php7.3-gd php7.3-dom php7.3-iconv php7.3-xsl php7.3-mbstring php7.3-ctype php7.3-zip php7.3-pdo php7.3-xml php7.3-bz2 php7.3-calendar php7.3-exif php7.3-fileinfo php7.3-json php7.3-mysqli php7.3-mysql php7.3-posix php7.3-tokenizer php7.3-xmlwriter php7.3-xmlreader php7.3-phar php7.3-soap php7.3-mysql php7.3-fpm libapache2-mod-php7.3 php7.3-gmp php7.3-bcmath php7.3-apcu php7.3-redis php7.3-imagick php7.3-imap php7.3-xdebug

```

&&    
```

apt-get -y install php7.4 php7.4-curl php7.4-intl php7.4-gd php7.4-dom php7.4-iconv php7.4-xsl php7.4-mbstring php7.4-ctype php7.4-zip php7.4-pdo php7.4-xml php7.4-bz2 php7.4-calendar php7.4-exif php7.4-fileinfo php7.4-json php7.4-mysqli php7.4-mysql php7.4-posix php7.4-tokenizer php7.4-xmlwriter php7.4-xmlreader php7.4-phar php7.4-soap php7.4-mysql php7.4-fpm libapache2-mod-php7.4 php7.4-gmp php7.4-bcmath php7.4-apcu php7.4-redis php7.4-imagick php7.4-imap php7.4-xdebug

```

&&   8.0
```

apt-get -y install php8.0 php8.0-curl php8.0-intl php8.0-gd php8.0-dom php8.0-mcrypt php8.0-iconv php8.0-xsl php8.0-mbstring php8.0-ctype php8.0-zip php8.0-pdo php8.0-xml php8.0-bz2 php8.0-calendar php8.0-exif php8.0-fileinfo php8.0-mysqli php8.0-mysql php8.0-posix php8.0-tokenizer php8.0-xmlwriter php8.0-xmlreader php8.0-phar php8.0-soap php8.0-mysql php8.0-fpm libapache2-mod-php8.0 php8.0-gmp php8.0-bcmath php8.0-apcu php8.0-redis php8.0-imagick php8.0-imap php8.0-xdebug

```

&&  8.1
```

apt-get -y install php8.1 php8.1-curl php8.1-intl php8.1-gd php8.1-xml php8.1-common php8.1-xsl php8.1-mbstring php8.1-zip php8.1-xml php8.1-bz2 php8.1-common php8.1-phpdbg php8.1-mysql php8.1-fpm php8.1-cli php8.1-cgi libphp8.1-embed libapache2-mod-php8.1 php8.1-mailparse php8.1-xdebug php8.1-imap php8.1-imagick php8.1-redis php8.1-apcu php8.1-bcmath php8.1-gmp php8.1-soap

```
&&

sudo add-apt-repository ppa:ondrej/php
sudo apt-get update

5.6
```

apt-get -y install php5.6 php5.6-curl php5.6-intl php5.6-gd php5.6-dom php5.6-mcrypt php5.6-iconv php5.6-xsl php5.6-mbstring php5.6-ctype php5.6-zip php5.6-pdo php5.6-xml php5.6-bz2 php5.6-calendar php5.6-exif php5.6-fileinfo php5.6-json php5.6-mysqli php5.6-mysql php5.6-posix php5.6-tokenizer php5.6-xmlwriter php5.6-xmlreader php5.6-phar php5.6-soap php5.6-mysql php5.6-fpm libapache2-mod-php5.6 php5.6-gmp php5.6-bcmath php5.6-apcu php5.6-redis php5.6-imagick php5.6-imap php5.6-xdebug

```

&&   7.0 
```

apt-get -y install php7.0 php7.0-curl php7.0-intl php7.0-gd php7.0-dom php7.0-mcrypt php7.0-iconv php7.0-xsl php7.0-mbstring php7.0-ctype php7.0-zip php7.0-pdo php7.0-xml php7.0-bz2 php7.0-calendar php7.0-exif php7.0-fileinfo php7.0-json php7.0-mysqli php7.0-mysql php7.0-posix php7.0-tokenizer php7.0-xmlwriter php7.0-xmlreader php7.0-phar php7.0-soap php7.0-mysql php7.0-fpm libapache2-mod-php7.0 php7.0-gmp php7.0-bcmath php7.0-apcu php7.0-redis php7.0-imagick php7.0-imap php7.0-xdebug

```

&&   7.1 
```

apt-get -y install php7.1 php7.1-curl php7.1-intl php7.1-gd php7.1-dom php7.1-mcrypt php7.1-iconv php7.1-xsl php7.1-mbstring php7.1-ctype php7.1-zip php7.1-pdo php7.1-xml php7.1-bz2 php7.1-calendar php7.1-exif php7.1-fileinfo php7.1-json php7.1-mysqli php7.1-mysql php7.1-posix php7.1-tokenizer php7.1-xmlwriter php7.1-xmlreader php7.1-phar php7.1-soap php7.1-mysql php7.1-fpm libapache2-mod-php7.1 php7.1-gmp php7.1-bcmath php7.1-apcu php7.1-redis php7.1-imagick php7.1-imap php7.1-xdebug

```

&&     7.2 
```

apt-get -y install php7.2 php7.2-curl php7.2-intl php7.2-gd php7.2-dom php7.2-iconv php7.2-xsl php7.2-mbstring php7.2-ctype php7.2-zip php7.2-pdo php7.2-xml php7.2-bz2 php7.2-calendar php7.2-exif php7.2-fileinfo php7.2-json php7.2-mysqli php7.2-mysql php7.2-posix php7.2-tokenizer php7.2-xmlwriter php7.2-xmlreader php7.2-phar php7.2-soap php7.2-mysql php7.2-fpm libapache2-mod-php7.2 php7.2-gmp php7.2-bcmath php7.2-apcu php7.2-redis php7.2-imagick php7.2-imap php7.2-xdebug

```

&&  7.3
```

apt-get -y install php7.3 php7.3-curl php7.3-intl php7.3-gd php7.3-dom php7.3-iconv php7.3-xsl php7.3-mbstring php7.3-ctype php7.3-zip php7.3-pdo php7.3-xml php7.3-bz2 php7.3-calendar php7.3-exif php7.3-fileinfo php7.3-json php7.3-mysqli php7.3-mysql php7.3-posix php7.3-tokenizer php7.3-xmlwriter php7.3-xmlreader php7.3-phar php7.3-soap php7.3-mysql php7.3-fpm libapache2-mod-php7.3 php7.3-gmp php7.3-bcmath php7.3-apcu php7.3-redis php7.3-imagick php7.3-imap php7.3-xdebug

```
 
&&  7.4
```

apt-get -y install php7.4 php7.4-curl php7.4-intl php7.4-gd php7.4-dom php7.4-iconv php7.4-xsl php7.4-mbstring php7.4-ctype php7.4-zip php7.4-pdo php7.4-xml php7.4-bz2 php7.4-calendar php7.4-exif php7.4-fileinfo php7.4-json php7.4-mysqli php7.4-mysql php7.4-posix php7.4-tokenizer php7.4-xmlwriter php7.4-xmlreader php7.4-phar php7.4-soap php7.4-mysql php7.4-fpm libapache2-mod-php7.4 php7.4-gmp php7.4-bcmath php7.4-apcu php7.4-redis php7.4-imagick php7.4-imap php7.4-xdebug

```

&&  8.0 
```

apt-get -y install php8.0 php8.0-curl php8.0-intl php8.0-gd php8.0-xml php8.0-common php8.0-xsl php8.0-mbstring php8.0-zip php8.0-xml php8.0-bz2 php8.0-common php8.0-phpdbg php8.0-mysql php8.0-fpm php8.0-cli php8.0-cgi libphp8.0-embed libapache2-mod-php8.0 php8.0-mailparse php8.0-xdebug php8.0-imap php8.0-imagick php8.0-redis php8.0-apcu php8.0-bcmath php8.0-gmp php8.0-soap php8.0-mysqli php8.0-pdo php8.0-pdo-mysql php8.0-fpm

```

&&  8.1
```

apt-get -y install php8.1 php8.1-curl php8.1-intl php8.1-gd php8.1-xml php8.1-common php8.1-xsl php8.1-mbstring php8.1-zip php8.1-xml php8.1-bz2 php8.1-common php8.1-phpdbg php8.1-mysql php8.1-fpm php8.1-cli php8.1-cgi libphp8.1-embed libapache2-mod-php8.1 php8.1-mailparse php8.1-xdebug php8.1-imap php8.1-imagick php8.1-redis php8.1-apcu php8.1-bcmath php8.1-gmp php8.1-soap php8.1-mysqli php8.1-pdo php8.1-pdo-mysql php8.1-xml php8.1-zip

```

&&  8.2
```

apt-get -y install php8.2 php8.2-curl php8.2-intl php8.2-gd php8.2-xml php8.2-common php8.2-xsl php8.2-mbstring php8.2-zip php8.2-xml php8.2-bz2 php8.2-common php8.2-phpdbg php8.2-mysql php8.2-fpm php8.2-cli php8.2-cgi libphp8.2-embed libapache2-mod-php8.2 php8.2-mailparse php8.2-xdebug php8.2-imap php8.2-imagick php8.2-redis php8.2-apcu php8.2-bcmath php8.2-gmp php8.2-soap php8.2-mysqli php8.2-pdo php8.2-pdo-mysql
```

&&  8.3
```

apt-get -y install php8.3 php8.3-curl php8.3-intl php8.3-gd php8.3-xml php8.3-common php8.3-xsl php8.3-mbstring php8.3-zip php8.3-xml php8.3-bz2 php8.3-common php8.3-phpdbg php8.3-mysql php8.3-fpm php8.3-cli php8.3-cgi libphp8.3-embed libapache2-mod-php8.3 php8.3-mailparse php8.3-xdebug php8.3-imap php8.3-imagick php8.3-redis php8.3-apcu php8.3-bcmath php8.3-gmp php8.3-soap php8.3-mysqli php8.3-pdo php8.3-pdo-mysql

```

&&   8.4
```

apt-get -y install php8.4 php8.4-curl php8.4-intl php8.4-gd php8.4-xml php8.4-common php8.4-xsl php8.4-mbstring php8.4-zip php8.4-xml php8.4-bz2 php8.4-common php8.4-phpdbg php8.4-mysql php8.4-fpm php8.4-cli php8.4-cgi libphp8.4-embed libapache2-mod-php8.4 php8.4-mailparse php8.4-xdebug php8.4-imap php8.4-imagick php8.4-redis php8.4-apcu php8.4-bcmath php8.4-gmp php8.4-soap php8.4-mysqli php8.4-pdo php8.4-pdo-mysql

```

2. PHP version change using stander users enable,disable, restart, switch version. 
``` shell 
Please follow the process.  
To change PHP version you need to disable one PHP version first then you need to enable second PHP version.  
commands are given below-  
to disable a php version - sudo a2dismod php<version>  
to enable a php version - sudo a2enmod php<version>  
you need to restart Apache services every time once you will switch PHP version.  
the command to restart apache services is given below -  
sudo /etc/init.d/apache2 restart  
you need to enable only one PHP version at a time.  
and you can check enabled PHP version using info.php file, in the terminal if you will check PHP version it will show the highest version installed.  
I have provided you access to update PHP alternatives using the command, you can set alternative of PHP according to the PHP version you have enabled.  
sudo update-alternatives --set php /usr/bin/php<version>
sudo update-alternative
```

use the manage apache2 services.
``` shell
You can use the following commands to manage Apache2 services.

Start the Apache2 service.

sudo systemctl start apache2.service

Restart the service.

sudo systemctl restart apache2.service

Stop the service.

sudo systemctl stop apache2.service

Enable the service.

sudo systemctl enable apache2.service

Disable the service.

sudo systemctl disable apache2.service
```

``` shell
Please follow the process.  
  
To change PHP version you need to disable one PHP version first then you need to enable second PHP version.  
  
commands are given below-  
  
to disable a php version - sudo a2dismod php<version>  
  
to enable a php version - sudo a2enmod php<version>  
  
you need to restart Apache services every time once you will switch PHP version.  
  
the command to restart apache services is given below -  
  
sudo /etc/init.d/apache2 restart  
  
you need to enable only one PHP version at a time.  
  
and you can check enabled PHP version using info.php file, in the terminal if you will check PHP version it will show the highest version installed.  
  
I have provided you access to update PHP alternatives using the command, you can set alternative of PHP according to the PHP version you have enabled.  
  
sudo update-alternatives --set php /usr/bin/php<version>
```