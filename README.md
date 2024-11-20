<h1>How to Install WSL & Ubuntu</h1>

```console
wsl --install --no-distribution
```
```console
wsl --list --online
```
```console
wsl --install -d Ubuntu-24.04
```
```console
sudo apt update && sudo apt full-upgrade -y
```
<h1>How to Install & setup docker</h1>
Download link: https://www.docker.com/products/docker-desktop
<h1>How to buy/use vps</h1>
Link: https://pq.hosting/?from=893755

Payment: Crypto Friendly

Putty: https://www.putty.org

<h1>How to use any free terminals</h1>
(1) https://shell.cloud.google.com/?hl=en_US&fromcloudshell=true&show=terminal

(2) https://gitpod.io/workspaces
(3) https://play.google.com/store/apps/details?id=com.termux
<h1>Learn About Basic Commands/Packages</h1>
Before any installation, you must update your packages

```console
sudo apt-get update && sudo apt-get upgrade -y
```

Main Packages

```console
sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
```

Python3, pip

```console
## Python 3.8 Pip, Python3 Install
sudo apt install -y python3-pip
sudo apt install pip
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev
```

NodeJS , npm, yarn

```console
# Check Nodejs Version
node --version
# if 18, skip nodejs steps

# Delete Nodejs old files
sudo apt-get remove nodejs
sudo apt-get purge nodejs
sudo apt-get autoremove
sudo rm /etc/apt/keyrings/nodesource.gpg
sudo rm /etc/apt/sources.list.d/nodesource.list

# Install Nodejs 18
NODE_MAJOR=18
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings

curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg

echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_${NODE_MAJOR}.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list

sudo apt-get update
sudo apt-get install -y nodejs
node --version

# Install npm
sudo apt-get install npm
npm --version

# Install yarn
curl -sSL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update -y
sudo apt-get install yarn -y
```

Docker, Docker-Compose

```console
sudo apt update -y && sudo apt upgrade -y
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt update -y && sudo apt upgrade -y

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Test Docker
sudo docker run hello-world
```

htop

```console
# Install
sudo apt install htop

# Run
htop
```

lsof, ufw

```console
# ports in-use
lsof -i -P -n | grep LISTEN

# What process is using port 80
lsof -i :80

# Open ports for external usage
sudo ufw allow <port>

# Example: Open port 3000
sudo ufw allow 3000
```

git

```console
# Transfer a github repository into linux
git clone https://github.com/FEdanish/Beginners-Node-RUN-guides
```

Go to home , root directory

```console
cd
```

Close screen

```console
CTRL + A + D
```
<h1>How to solve any errors (Self dependent)</h1>

(1) ChatGPT: https://chatgpt.com
(2) FE PVT GROUP



