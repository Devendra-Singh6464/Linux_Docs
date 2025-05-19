
```shell
#!/bin/bash

#curl -sL [https://deb.nodesource.com/setup_22.x](https://deb.nodesource.com/setup_22.x) | sudo -E bash -  
curl -sL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt-get install nodejs -y
apt-get install nsolid -y 
nvm install 22
node -v
npm -v
```
https://nodejs.org/en/download


go to root and paste this:
```shell
curl -sL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt-get install -y nodejs
```

If your install older node version in mac os then.
for mac manually download .pkg package.
- Note: before download .pkg package remove node or nvm.
check this website. https://nodejs.org/en/blog/release/v14.21.3
```link
https://nodejs.org/en/blog/release/v14.21.3
```

```shell
curl -o node-v14.21.3.pkg https://nodejs.org/dist/v14.21.3/node-v14.21.3.pkg
```

```shell
sudo installer -pkg node-v14.21.3.pkg -target /
```

```shell
curl -o node-v18.20.5.pkg https://nodejs.org/dist/v18.20.5/node-v18.20.5.pkg
```

```shell
sudo installer -pkg node-v18.20.5.pkg -target /
```


