
```bash
#!/bin/sh

sudo apt-get install curl gnupg apt-transport-https -y

## Team RabbitMQ's main signing key
curl -1sLf "https://keys.openpgp.org/vks/v1/by-fingerprint/0A9AF2115F4687BD29803A206B73A36E6026DFCA" | sudo gpg --dearmor | sudo tee /usr/share/keyrings/com.rabbitmq.team.gpg > /dev/null
## Community mirror of Cloudsmith: modern Erlang repository
curl -1sLf https://github.com/rabbitmq/signing-keys/releases/download/3.0/cloudsmith.rabbitmq-erlang.E495BB49CC4BBE5B.key | sudo gpg --dearmor | sudo tee /usr/share/keyrings/rabbitmq.E495BB49CC4BBE5B.gpg > /dev/null
## Community mirror of Cloudsmith: RabbitMQ repository
curl -1sLf https://github.com/rabbitmq/signing-keys/releases/download/3.0/cloudsmith.rabbitmq-server.9F4587F226208342.key | sudo gpg --dearmor | sudo tee /usr/share/keyrings/rabbitmq.9F4587F226208342.gpg > /dev/null

## Add apt repositories maintained by Team RabbitMQ
sudo tee /etc/apt/sources.list.d/rabbitmq.list <<EOF
## Provides modern Erlang/OTP releases
##
deb [signed-by=/usr/share/keyrings/rabbitmq.E495BB49CC4BBE5B.gpg] https://ppa1.novemberain.com/rabbitmq/rabbitmq-erlang/deb/ubuntu jammy main
deb-src [signed-by=/usr/share/keyrings/rabbitmq.E495BB49CC4BBE5B.gpg] https://ppa1.novemberain.com/rabbitmq/rabbitmq-erlang/deb/ubuntu jammy main

# another mirror for redundancy
deb [signed-by=/usr/share/keyrings/rabbitmq.E495BB49CC4BBE5B.gpg] https://ppa2.novemberain.com/rabbitmq/rabbitmq-erlang/deb/ubuntu jammy main
deb-src [signed-by=/usr/share/keyrings/rabbitmq.E495BB49CC4BBE5B.gpg] https://ppa2.novemberain.com/rabbitmq/rabbitmq-erlang/deb/ubuntu jammy main

## Provides RabbitMQ
##
deb [signed-by=/usr/share/keyrings/rabbitmq.9F4587F226208342.gpg] https://ppa1.novemberain.com/rabbitmq/rabbitmq-server/deb/ubuntu jammy main
deb-src [signed-by=/usr/share/keyrings/rabbitmq.9F4587F226208342.gpg] https://ppa1.novemberain.com/rabbitmq/rabbitmq-server/deb/ubuntu jammy main

# another mirror for redundancy
deb [signed-by=/usr/share/keyrings/rabbitmq.9F4587F226208342.gpg] https://ppa2.novemberain.com/rabbitmq/rabbitmq-server/deb/ubuntu jammy main
deb-src [signed-by=/usr/share/keyrings/rabbitmq.9F4587F226208342.gpg] https://ppa2.novemberain.com/rabbitmq/rabbitmq-server/deb/ubuntu jammy main
EOF

## Update package indices
sudo apt-get update -y

## Install Erlang packages
sudo apt-get install -y erlang-base \
                        erlang-asn1 erlang-crypto erlang-eldap erlang-ftp erlang-inets \
                        erlang-mnesia erlang-os-mon erlang-parsetools erlang-public-key \
                        erlang-runtime-tools erlang-snmp erlang-ssl \
                        erlang-syntax-tools erlang-tftp erlang-tools erlang-xmerl

## Install rabbitmq-server and its dependencies
sudo apt-get install rabbitmq-server -y --fix-missing
```


After that 
```shell
sudo systemctl status rabbitmq-server
sudo systemctl restart rabbitmq-server
```


```shell
sudo vi /etc/rabbitmq/rabbitmq.conf
```
 
  -   If `rabbitmq.conf` does not exist, create it.
  -  Paste these lines into `/etc/rabbitmq/rabbitmq.conf`
```shell
listeners.tcp.default = 5672
management.listener.port = 15672
```

- Enable RabbitMQ Management Plugin
```shell
sudo rabbitmq-plugins enable rabbitmq_management
```
- rabbitmqctl add_user new_user pass

Create new RabbitMQ user having the username _new_user_ and the password _pass_.
syntax: 
`rabbitmqctl add_user new_user pass`
`rabbitmqctl set_user_tags new_user administrator`
- Create new RabbitMQ user having the username _new_user_ and the password _pass_.
```shell
rabbitmqctl add_user admin admin
```

- Add _administrator_ tag to the newly created user _new_user_ i.e. make _new_user_ an _administrator_.
```shell
sudo rabbitmqctl set_user_tags admin administrator
```

- Add _administrator_ tag to the newly created user _new_user_ i.e. make _new_user_ an _administrator_.
```shell
rabbitmqctl list_users
```

- Grant full _configure_, _write_ and _read_ permissions to the user _new_user_ within the virtual host “/”. The generic command is
$ set_permissions [-p vhost] user conf write read, where conf, write and read
are regular expressions matching resources names for which the user is granted _configure_, _write_ and _read_ permissions respectively.

$ rabbitmqctl list_permissions -p /
```shell
rabbitmqctl set_permissions -p / admin ".*" ".*" ".*"
```

Reference
https://www.orangehrm.com/assets/Files/OrangeHRM-RabbitMQ-Installation-Guide-Ubuntu.pdf
https://www.algotech.solutions/shorts/rabbitmq-create-new-user/