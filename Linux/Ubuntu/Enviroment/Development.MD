# Basic config for initial developer enviroment

## NodeJS

```bash
# Installing node version 14.17.0

curl -fsSL https://deb.nodesource.com/setup_14.x | sudo -E bash -

sudo apt-get install -y nodejs

node -v
```

## Yarn

```bash
# Installing yarn latest

sudo npm install -g yarn

yarn -v

```

## GIT

```bash
# Installing git latest

sudo apt update

sudo apt install git

git --version

```

## Docker

```bash
# Installing docker latest

sudo apt update

sudo apt install apt-transport-https ca-certificates curl software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

sudo apt update

apt-cache policy docker-ce

sudo apt install docker-ce

sudo systemctl status docker

# Execute docker without sudo

sudo usermod -aG docker ${USER}

su - ${USER}

id -nG

sudo usermod -aG docker username

docker -v
```
