# How To Set Up Alephium Fullstack on a Linux Machine

This tutorial will guide you through setting up the Alephium Fullstack, consisting of Node, Explorer Backend, and Explorer Frontend, on a Linux machine. This setup has been successfully tested on a Raspberry Pi 4 Model B running Debian 12.6.

## Prerequisites

- A Linux machine (e.g., Raspberry Pi 4 Model B running Debian 12.6)
- Basic knowledge of terminal commands

## Steps

### 1. Install Docker
If Docker is not already installed on your machine, run the following command to install it:

```
 curl -sSL https://get.docker.com | sh
```

### 2. Add Your User to the Docker Group
To manage Docker as a non-root user, add your user to the Docker group:

```
sudo usermod -aG docker $USER
```
Log out and log back in for the changes to take effect.

### 3. Install Docker Compose
Install Docker Compose, a tool for defining and running multi-container Docker applications:

```
sudo apt-get install docker-compose -y
```

### 4. Clone the Alephium Fullstack Repository
Clone the Alephium Fullstack repository from GitHub:

```
git clone https://github.com/dm807cam/alephium-fullstack
```

### 5. Adjust machine's IP
Replace the hardcoded IPs at the bottom of the compose file

### 6. Start Alephium Fullstack with Docker Compose
Navigate to the cloned repository directory, set the host IP environment variable, and start the services:

```
cd alephium-fullstack
docker-compose up -d
```
This command will set up and run the Alephium Fullstack services in detached mode.

## Accessing the Services

- Node API Swagger: http://127.0.0.1:12973/docs
- Explorer API Swagger: http://${HOST_IP}:9090/docs
- Explorer Frontend: http://${HOST_IP}:3000
