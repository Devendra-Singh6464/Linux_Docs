All ansible modules 
https://docs.ansible.com/ansible/2.9/modules/modules_by_category.html

* Install Ansible 
 
``` shell
sudo apt install ansible -y
```

- If you facing this issue .
`ansible --version `
`ERROR: Ansible requires the locale encoding to be UTF-8; Detected ISO8859-1.`

1. Check Current Locale Settings.
``` shell
locale
```

2. Generate the UTF-8 Locale.
``` shell
sudo locale-gen en_US.UTF-8
```

3.  Set the Locale.
``` shell
export LC_ALL=en_IN.UTF-8
```

Add this line to your `~/.bashrc` or `~/.zshrc` file to make it permanent:
``` shell
echo 'export LC_ALL=en_IN.UTF-8' >> ~/.bashrc
```

``` shell
source ~/.bashrc
```

``` shell
ansible --version
```

- Check ansible man page[doc]
``` shell
ansible-doc -l 
```

- Check specific module commands.
``` shell
ansible-doc -l | grep docker
```

Run command with out using ansible playbook(script).
```shell 
ansible <host> -m <module> -a "<module arguments>"

ansible myhosts -m command -a "df -hT"
```

Using ping command
``` shell
ansible 192.168.121.204 -m ping 
```

Copy file to another server 
``` shell
ansible 192.168.121.204 -m copy -a "src=/home/users/devendra.singh/ansible_quickstart/devfile dest=/home/vagrant/"
```

another try.
``` shell
ansible 192.168.121.204 -m copy -a "src=/home/users/devendra.singh/ansible_quickstart/devfile dest=/home/vagrant/ mode=0777" -b --ask-become-pass
```

Syntax: 
``` shell syntax
-b => become
--ask-become-pass => <ask for the sudo password>
```

Restart service in server with out ansible playbook.
syntax.
``` shell
ansible <hosts> -m <module> -a <"service=name state=<state_type">
```

``` shell
ansible all -m service -a "name=nginx state=reloaded"
```

Run bash script in server if bash script already present in server.
``` shell
ansible all -m shell -a "/home/vagrant/test.sh"
```

Checks all tags in our ansible playbook.
```shell
ansible-playbook package_install.yml --list-tags
```

