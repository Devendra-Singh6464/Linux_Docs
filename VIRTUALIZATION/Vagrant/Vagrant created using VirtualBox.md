### Vagrant installation [https://developer.hashicorp.com/vagrant/install](https://developer.hashicorp.com/vagrant/install)

```shell
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vagrant
```

- After install vagrant check vagrant --version.

```shell
vagrant --version
```

![Screenshot from 2025-02-17 15-12-01.png](app://df9bc39667f38b2b0d3cba1c383be234f597/home/users/devendra.singh/myDocs/iNotes/Screenshot%20from%202025-02-17%2015-12-01.png?1739785321306)![vagrant_getting start.png](app://df9bc39667f38b2b0d3cba1c383be234f597/home/users/devendra.singh/myDocs/iNotes/vagrant_getting%20start.png?1739858405302)![vagrant_boxs.png](app://df9bc39667f38b2b0d3cba1c383be234f597/home/users/devendra.singh/myDocs/iNotes/vagrant_boxs.png?1739858446668)

- Initialize the project.

```shell
vagrant init ubuntu/focal64
```

Install Oracle Virtual box  https://www.virtualbox.org/wiki/Linux_Downloads
``` shell
dpkg -i virtualbox-7.1_7.1.6-167084~Ubuntu~jammy_amd64.deb 
```
```shell
sudo /sbin/vboxconfig
```
Install dependency.
``` shell
sudo apt update
sudo apt install build-essential gcc make perl dkms linux-headers-$(uname -r)
```
 Create a directory.
```shell
mkdir -p myvm/myvag
```
- change directory--
```shell
cd myvag 
```
Run this.
```shell
vagrant up --provider virtualbox
```


