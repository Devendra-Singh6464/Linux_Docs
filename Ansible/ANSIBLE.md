Reference link: https://docs.ansible.com/ansible/latest/

* Install Ansible
* To configure the PPA on your system and install Ansible run these commands:
``` shell
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install ansible
```

* Run the following commands to add the repository and install Ansible. Set `UBUNTU_CODENAME=...` based on the table above (we use `jammy` in this example).
```shell
UBUNTU_CODENAME=jammy
wget -O- "https://keyserver.ubuntu.com/pks/lookup?fingerprint=on&op=get&search=0x6125E2A8C77F2818FB7BD15B93C4A3FD7BB9C367" | sudo gpg --dearmour -o /usr/share/keyrings/ansible-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/ansible-archive-keyring.gpg] http://ppa.launchpad.net/ansible/ansible/ubuntu $UBUNTU_CODENAME main" | sudo tee /etc/apt/sources.list.d/ansible.list
sudo apt update && sudo apt install ansible
```

* Check ansible version.
``` shell
ansible --version
```

* Check ansible working fine.
``` shell
ansible loclhost -m ping 
```
If you saw this that's mean ansible working fine.: 
``` shell
localhost | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
```

* If `ansible.cfg` file already created so nice if not created so.
``` shell
ansible-config init --disable -t all > ansible.cfg
```

