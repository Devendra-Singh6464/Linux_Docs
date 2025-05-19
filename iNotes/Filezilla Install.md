1. Download the filezilla (https://filezilla-project.org/download.php).
2. extract the file.
```
tar -xvf FileZilla_3.67.1_x86_64-linux-gnu.tar.xz
```
3. Run Filezilla a terminal.
```
vi ./bin/filezilla
```
4. Create Symblink.
```
sudo ln -s /opt/filezilla3/bin/filezilla /usr/bin/filezilla
```
5. Verify 
```
ls -l /usr/bin/filezilla
```
This should show something like:
```
/usr/bin/filezilla -> /opt/filezilla3/bin/filezilla
```
6. Create a `.desktop` file for Filezilla:
```
sudo vi /usr/share/applications/filezilla.desktop
```
and paste this:
```
[Desktop Entry]
Name=FileZilla
Comment=FileZilla FTP Client
Exec=/path/to/extracted/FileZilla3/bin/filezilla
Icon=/path/to/extracted/FileZilla3/share/icons/hicolor/48x48/apps/filezilla.png
Terminal=false
Type=Application
Categories=Network;
```

#!/bin/bash

wget 192.168.1.32/filezilla.tar.xz
tar -xvf filezilla.tar.xz -C /opt/
ln -sf /opt/FileZilla3/bin/filezilla /usr/bin/filezilla
	