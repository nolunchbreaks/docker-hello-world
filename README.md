# Docker-hello-world
Docker on an AWS Ubuntu instance and run a simple Hello World application:
[![LinkedIn](https://img.shields.io/badge/Connect%20with%20me%20on-LinkedIn-blue.svg)](https://www.linkedin.com/in/osagie-anolu-963b78216/)
[![GitHub](https://img.shields.io/github/stars/AmanPathak-DevOps.svg?style=social)](https://github.com/nolunchbreaks)





# Docker on AWS Ubuntu Instance

This guide provides step-by-step instructions to install Docker on an AWS Ubuntu instance and run a simple "Hello World" application.

# Prerequisites

- An AWS account
- An Ubuntu instance running on AWS EC2
- SSH access to the instance

# Step 1: Connect to Your Instance

- Open your terminal.
-  Connect to your AWS Ubuntu instance using SSH:
   ```sh
   ssh -i "your-key.pem" ec2-user@your-instance-ip
- Step 2: Update Ubuntu Package List

# Run the following commands to update your package list and upgrade existing packages:

- sudo apt update
- sudo apt upgrade -y
- sudo apt install docker.io

# Start Docker and Enable it to run on boot
- sudo systemctl start docker
- sudo systemctl enable docker

# Verify Docker Installation
- docker --version

# Run Docker without sudo
- sudo usermod -aG docker $USER
  - Log out and log back in, or restart your instance for the changes to take effect.
  - newgrp docker

# Test Docker
Test Docker by running a simple container:
- sudo docker run hello-world
- Running a Hello World Nginx Container
- Run the Nginx container:

# Create a directory for your project
- mkdir hello-world-docker
- cd hello-world-docker

# create a file
- nano index.html
- add a simple html code to the file
# create docker file
- nano dockerfile

# build docker image
-docker build -t hello-world-nginx
![Screenshot (2)](https://github.com/user-attachments/assets/2e01851d-2b60-4f9e-b8b0-cfc8181ac4eb)
