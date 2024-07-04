## 1. Install Docker and Docker-Compose

You can still install Docker on a Linux Server that is not running Ubuntu, however, this may require different commands!

### 1.1. Install Docker
```bash
sudo apt update

sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

sudo apt update

sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### 1.2. Check if Docker is installed correctly
```bash
sudo docker run hello-world
```

### 1.3. Install Docker-Compose

Download the latest version (in this case it is 1.25.5, this may change whenever you read this tutorial!)

```bash
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
```

### 1.4. Check if Docker-Compose is installed correctly
```bash
sudo docker-compose --version
```

### 1.5. (optional) Add your linux user to the `docker` group
```bash
sudo usermod -aG docker $USER
```

### automatically start the Docker container system
```bash
sudo systemctl enable docker.service 
```

## Installation

Run docker containers <br>
```docker compose up -d```