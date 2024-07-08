# docker_springboot_mysql

## Intall Docker and Docker Compose
vi install-docker.sh  

#!/bin/bash<br />
sudo apt update  
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common__
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg  
echo "deb [signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null  
sudo apt update  
sudo apt install -y docker-ce  
sudo systemctl start docker  
sudo systemctl enable docker  
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose  
sudo chmod +x /usr/local/bin/docker-compose  
docker --version  
docker-compose --version  

chmod +x install-docker.sh  
sh install-docker.sh  

## Pull docker images
docker pull kienkt/shoeshop_app:v2  
docker pull kienkt/shoeshop_mysql:v2  

## Run docker-compose 
vi docker-compose.yml  
Copy file docker-compose.yml and run:  
docker-compose up -d
