
Go to this path
```shell
cd /home/<users>/www/html/
```

Download the Bagisto zip file
``` shell
wget https://codeload.github.com/bagisto/bagisto/legacy.zip/refs/tags/v2.2.4
```

Extract download file in my case file name`v2.2.4`.
```shell
unzip v2.2.4
```

Go extract bagisto file
```shell
cd www/html/bagisto
```

Install Composer
```shell
sudo apt install composer
```

install php version above 8.
```shell
apt-get -y install php8.2 php8.2-curl php8.2-intl php8.2-gd php8.2-xml php8.2-common php8.2-xsl php8.2-mbstring php8.2-zip php8.2-xml php8.2-bz2 php8.2-common php8.2-phpdbg php8.2-mysql php8.2-fpm php8.2-cli php8.2-cgi libphp8.2-embed libapache2-mod-php8.2 php8.2-mailparse php8.2-xdebug php8.2-imap php8.2-imagick php8.2-redis php8.2-apcu php8.2-bcmath php8.2-gmp php8.2-soap php8.2-mysqli php8.2-pdo php8.2-pdo-mysql
```
insurer to mysql installed in your server.
Create Bagisto data base
```shell
Create database bagisto;
```
