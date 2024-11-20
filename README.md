<h1>How to Install WSL & Ubuntu</h1>

<pre>wsl --install --no-distribution</pre>
<pre>wsl --list --online</pre>
<pre>wsl --install -d Ubuntu-24.04</pre>
<pre>sudo apt update && sudo apt full-upgrade -y</pre>
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
<pre>sudo apt-get update && sudo apt-get upgrade -y</pre>
Main Packages
<pre>sudo apt install curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y</pre>
Python3, pip
<pre>## Python 3.8 Pip, Python3 Install
sudo apt install -y python3-pip
sudo apt install pip
sudo apt install -y build-essential libssl-dev libffi-dev python3-dev</pre>
Go
<pre>sudo rm -rf /usr/local/go
curl -L https://go.dev/dl/go1.22.3.linux-amd64.tar.gz | sudo tar -xzf - -C /usr/local
echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bash_profile
source .bash_profile
go version</pre>
NodeJS , npm, yarn
<pre># Check Nodejs Version
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
sudo apt-get install yarn -y</pre>

