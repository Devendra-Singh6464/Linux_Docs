### Vagrant installation https://developer.hashicorp.com/vagrant/install

```shell 
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vagrant
```
- After install vagrant check vagrant --version.
``` shell
vagrant --version
```
![[Screenshot from 2025-02-17 15-12-01.png]]
![[vagrant_getting start.png]]
![[vagrant_boxs.png]]

- Create a directory.
``` shell
mkdir -p myvm/myvag
```
- change directory--
``` shell
cd myvag 
```
- Initialize the project.
``` shell
vagrant init ubuntu/focal64
```

``` shell
vi Vagrantfile
```
*Default Vagrantfile using `vagrant init` *
``` shell 
# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "base"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Disable the default share of the current code directory. Doing this
  # provides improved isolation between the vagrant box and your host
  # by making sure your Vagrantfile isn't accessible to the vagrant box.
  # If you use this you may want to enable additional shared subfolders as
  # shown above.
  # config.vm.synced_folder ".", "/vagrant", disabled: true

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
```
*Note: If you want to with out GUI using this machine so install libvirt*
Install KVM
``` shell
sudo apt install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils
```
 Start the KVM services.
``` shell
sudo systemctl enable --now libvirtd
```

1. install libvirt
``` shell
sudo apt-get purge vagrant-libvirt
sudo apt-mark hold vagrant-libvirt
sudo apt-get update && \
    sudo apt-get install -y qemu libvirt-daemon-system ebtables libguestfs-tools \
        vagrant ruby-fog-libvirt
```
2. Install the latest release of vagrant-libvirt
``` shell
vagrant plugin install vagrant-libvirt
```

**Check If You Have Access to libvirt-sock**
``` shell
ls -lah /var/run/libvirt/libvirt-sock
```
If you see this output that's mean your user don't have libvirt permissions
``` shell
srw-rw---- 1 root libvirt 0 Feb 4 12:34 /var/run/libvirt/libvirt-sock
```

Then only **root and `libvirt` group members** can access it.

added yourself to the `libvirt` group using and restart your system:
``` shell
sudo usermod -aG libvirt devendra.singh
```

- Vagrant file after updated.
``` shell
# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "generic/rhel9"
  config.vm.box_version = "4.3.12"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Disable the default share of the current code directory. Doing this
  # provides improved isolation between the vagrant box and your host
  # by making sure your Vagrantfile isn't accessible to the vagrant box.
  # If you use this you may want to enable additional shared subfolders as
  # shown above.
  # config.vm.synced_folder ".", "/vagrant", disabled: true

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
#    config.vm.provider "virtualbox" do |vb|
    config.vm.provider "libvirt" do |libvirt|

  #   # Display the VirtualBox GUI when booting the machine
  #   libvirt.gui = false
  #
  #   # Customize the amount of memory on the VM:
      libvirt.memory = "2048"
      libvirt.cpus = 2
    end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
```
- edit this line and " write name of your box"
``` shell
config.vm.box = "ubuntu/focal64"
```
- like this. starting the file.
``` shell
# Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "ubuntu/focal64"
```
- changed.
``` shell
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.box_version = "20240821.0.1"
end
```
- Install a box vagrant box add [ubuntu 22.04].
``` shell
vagrant box add generic/ubuntu2204
```

 If your want install another box so https://portal.cloud.hashicorp.com/vagrant/discover visit this link and select. and install  
 - Up machine using libvirt
``` shell
vagrant up --provider=libvirt
```
 vagrant machine ssh
``` shell
vagrant ssh
```

``` shell
vagrant up
```

- Check syntax correct 
``` shell
vagrant provision
```

- check vagrant status.
``` shell
vagrant status 
```
- stop vagrant machine.
``` shell
vagrant halt
```
- List installed vagrant boxs.
``` shell 
vagrant box list
```
- remove box 
``` shell
vagrant box remove [box-name]
```
- Destroy machine forcefully.
``` shell
vagrant destroy -f
```


## Port Forwarding
Networking allows access to the Virtual machine from outside(like from the host system).
Vagrant by default forwards port 22 from the guest machine (VM) to an open in the machine.

* Step 1 - Open vagrantfile and add this line.
``` shell
config.vm.network "forwarded_port", guest:80, host:8080
```
- Step 2 - Restart VM if your any changes with Vagrantfile. 
``` shell
vagrant reload --provision
```
- Step 3 - open the browser.
``` shell
localhost:8080 
```
- If port 8080 is busy:
step 4 - Add auto-correction option ```auto_correct:true``` in Vagrantfile 
by default, Vagrant will choose auto-correction port between port 2200 and port 2250 range.

## Assigned the IP-
- DHCP
Configure a bridge network with DHCP.
``` shell
config.vm.network "public_network", bridge: "your_network_interface", type: "dhcp"
```
- Static IP.
``` shell
config.vm.network "public_network", dev: "en0p1:", ip: "192.168.5.195"
```
- Vagrant default password.
``` shell
vagrant
```
- Create vagrant box.
``` shell
vagrant package
```
Routing:
*If  your in the vagrant and then you you can't ping in assigned network then add route*
*route add in vagrant all networks*
``` shell
vagrant@ubuntu2204:~# sudo route add -net 192.168.25.0 netmask 255.255.255.0 gateway 192.168.5.1
```

If you add routing in vagrant server then made some configuration in `/etc/rc.local`
``` shell
vi /etc/rc.loacl
```
add this line in `rc.local` file.
``` shell
#!/bin/sh -e
#
# rc.local - Executed at the end of each multiuser runlevel

# Add persistent route
/sbin/route add -net 192.168.10.0 netmask 255.255.255.0 gw 192.168.5.1

exit 0
```
``` shell
sudo chmod +x /etc/rc.local
```
`gw: vagrant default gateway, 192.168.10.0 your provided network range`.

After this create rc.local systemd service.
``` shell
sudo vi /etc/systemd/system/rc-local.service
```
add this configuration in the file.
```shell
[Unit]
Description=/etc/rc.local Compatibility
ConditionPathExists=/etc/rc.local

[Service]
Type=forking
ExecStart=/etc/rc.local start
TimeoutSec=0
StandardOutput=tty
RemainAfterExit=yes
SysVStartPriority=99

[Install]
WantedBy=multi-user.target
```
Restart the services.
``` shell
sudo systemctl enable rc-local
sudo systemctl start rc-local
```


## Share Vagrant-box
`NOTE: Copy the Vagrant package to the machine of the user you want to give the Vagrant machine to.`

Reference link:
https://grahamhelton.com/blog/vagrant/
https://vagrant-libvirt.github.io/vagrant-libvirt/  
https://developer.hashicorp.com/vagrant/install  
https://www.youtube.com/playlist?list=PLhW3qG5bs-L9S272lwi9encQOL9nMOnRa  

