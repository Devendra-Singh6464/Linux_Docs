*all Postman version*
``` shell
https://www.postman.com/release-notes/postman-app/
```

``` shell
!/bin/bash
wget https://dl.pstmn.io/download/version/9.31.0/linux64 -O postman.tar.gz
sudo tar -xzf postman.tar.gz -C /opt
rm postman.tar.gz
sudo ln -sf /opt/Postman/Postman /usr/bin/postman
cat > /usr/share/applications/postman.desktop <<EOL
[Desktop Entry]
Encoding=UTF-8
Name=Postman
Exec=postman
Icon=/opt/Postman/app/resources/app/assets/icon.png
Terminal=false
Type=Application
Categories=Development;
EOL
```
*If you want to update postman so*
* Note: go to `/opt/` and rename old postman file like `mv postman postman.old` the untar new postman file and in these location.


``` shell postman specific version
https://dl.pstmn.io/download/version/9.31.0/linux64
```

```shell
https://dl.pstmn.io/download/latest/linux64
```
