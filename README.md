# docker-laravel
Basic docker configuration for Laravel (or any framework).

## docker preparation
* apt update && apt upgrade -y
* sudo apt-get install ca-certificates curl gnupg
* sudo install -m 0755 -d /etc/apt/keyrings
* curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
* sudo chmod a+r /etc/apt/keyrings/docker.gpg
* echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
* sudo apt-get update

## docker instalation
* sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
* sudo systemctl status docker
* docker --version
* you are ready to go

## reminder
* docker compose build
* docker compose up -d (add container name here to be specific)
* docker compose down (add container name here to be specific)
* docker restart (add container name here)

## reference
https://docs.docker.com/engine/install/ubuntu/