Some basics configurations for vagrant creation [60GB  box}.

`Vagrantfile` Configurations

``` shell
Vagrant.configure("2") do |config|
  
  config.vm.box = "http://192.168.25.209/ubuntu2060.box"
  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"

    config.vm.network "public_network", ip: "192.168.25.76"

    config.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
      vb.cpus = 2
end
```