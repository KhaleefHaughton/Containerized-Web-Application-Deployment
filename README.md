# Containerized-Web-Application-Deployment
Congrats, You Just Put Your Website in a Box 🎁 (Now Don’t Forget Where You Left It) 

A step-by-step guide for Dockerizing, deploying, and documenting a web application.

## Overview
This project demonstrates containerizing a website using Docker, deploying it, and documenting the entire development and deployment workflow in GitHub. The goal is to make the process repeatable and easy to understand.

## 📌 Table of Contents
1. [Project Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Architecture](#architecture)
4. [Setup Guide](#setup-guide)
5. [Deploying with Docker](#deploying-with-docker)
6. [Pushing Images to Docker Hub](#pushing-images-to-docker-hub)
7. [CI/CD Integration](#cicd-integration)
8. [Making Updates](#making-updates)
9. [Useful Commands](#useful-commands)


## 2. 🧰 Prerequisites
Before starting, ensure you have:
- Git installed on your machine
- A GitHub account
- Docker installed
- AWS account for cloud deployment


## 3. 🧱 Architecture
Web App Source → GitHub Repo → Docker Container → AWS Deployment



## 4. 🚀 Setup Guide

Clone the Repository
```
git clone https://github.com/KhaleefHaughton/containerized-web-deployment.git
cd containerized-web-deployment

```

## 5. 🐳 Docker Deployment Instructions
[Copy these steps verbadum]

```
sudo snap install docker
docker version
sudo chmod 666 /var/run/docker.sock

```

Login and Connect Docker
docker login

🐳 Deploying with Docker
Build the Docker image:
```bash
docker build -t my-webapp .

```
Click Nginx
Image 1.29.1
pull Docker image
docker pull nginx:1.29.1

## 6. Push Images to Docker Hub**

📦 Push to Docker Hub
1. Log in:*********
docker login

Run a Docker Ubuntu container running detached and on port 80

--name (gives the container a name)
-d (running it detached so it wont slow down production on the front end.)
-p (ports)

I named my image “web1” to keep track of it to refer back to
```
docker run -d -p 80:80 myweb1
```

Verify that the container is up and running
```
docker ps

```
Tag the image:
docker tag my_new_image_nginx alexanderfuse/my_new_nginx:V1
The output should be the latest

Push the image:
docker push alexanderfuse/my_new_nginx:V1


Identify the instance that I am in without going back to the AWS console.
```
curl -s ifconfig.me

```
I copied the IP and added port 8080 (3.80.160.152:8080)
Navigated into web browser and pasted the IP to make sure your container is up and running.

SUCCESS!






