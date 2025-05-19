1. Apache2 configure for wildcard domain
``` shell
<VirtualHost *:80>
       
        ServerName hotel-booking.com
        ServerAlias hotel-booking.com *.hotel-booking.com

        ServerAdmin webmaster@localhost
        DocumentRoot /home/users/devendra.singh/www/html/Hotel_Booking-PHP

        ErrorLog ${APACHE_LOG_DIR}/error.log
        CustomLog ${APACHE_LOG_DIR}/access.log combined

</VirtualHost>
```

2. Host-entry in `vi /etc/hosts`
``` shell
127.0.0.1       hotel-booking.com
127.0.0.1       *.hotel-booking.com
```

3. Install dnsmasq.
``` shell
sudo apt-get install dnsmasq
```

2. `cd /etc/dnsmasq.d` create a domain file like if your domain is `hotel-booking.com`  in this location.
``` shell
cd /etc/dnsmasq.d/
```

- Create file[domain name] and add this line.
``` shell
echo "address=/hotel-booking.com/127.0.0.1" > hotel-booking.com
```

3. Go to this file and make some changes and add on this lines 
``` shell
vi /etc/dnsmasq.conf
```

``` shell
port=5353
listen-address=127.0.0.1
address=/hotel-booking.com/127.0.0.1
```

4. Go this directory `/etc/NetworkManager/dnsmasq.d` and create this file domain name `hotel-booking.com-wildcard.conf` and add this line.
``` shell 
echo "address=/.hotel-booking.com/127.0.0.1" > hotel-booking.com-wildcard.conf
```

5.  Add this line in this location  `/etc/NetworkManager# vi NetworkManager.conf` 
``` shell
dns=dnsmasq
```

6. Made changes in `vi /etc/resolv.conf`
``` shell
nameserver 127.0.1.1
```

Let NetworkManager manage `/etc/resolv.conf`
``` shell
sudo rm /etc/resolv.conf ; sudo ln -s /var/run/NetworkManager/resolv.conf /etc/reso
```

7. also made changes in this file `vi /etc/systemd/resolved.conf`
``` shell
DNS=127.0.0.1
#FallbackDNS=
Domains=hotel-booking.com
```

7.  Restart apache, dnsmasq and network-manager service.
``` shell
sudo systemctl reload NetworkManager
sudo systemctl restart dnsmasq
sudo systemctl restart apache2
systemctl restart systemd-resolved.service
```

Reference link:
https://askubuntu.com/questions/1029882/how-can-i-set-up-local-wildcard-127-0-0-1-domain-resolution-on-18-04-20-04