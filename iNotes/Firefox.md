https://support.mozilla.org/en-US/kb/install-firefox-**linux

``` shell
#!/bin/bash

sudo snap remove firefox
apt remove --purge firefox
sudo apt autoremove -y
sudo install -d -m 0755 /etc/apt/keyrings

wget -q https://packages.mozilla.org/apt /repo-signing-key.gpg -O- | sudo tee /etc/apt/keyrings/packages.mozilla.org.asc > /dev/null

echo "deb [signed-by=/etc/apt/keyrings/packages.mozilla.org.asc] https://packages.mozilla.org/apt mozilla main" | sudo tee -a /etc/apt/sources.list.d/mozilla.list > /dev/null

echo '
Package: *
Pin: origin packages.mozilla.org
Pin-Priority: 1000
' | sudo tee /etc/apt/preferences.d/mozilla

sudo apt-get update && sudo apt-get install firefox -y
```