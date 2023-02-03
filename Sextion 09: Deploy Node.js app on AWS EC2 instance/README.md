# <h1 align=center> Deploy Node.js app on AWS EC2 instance <h1>

## What is Node.js?
- Node.js is a JavaScript runtime for server-side programming. 
- we can create scalable backend functionality using JavaScript  
  
## [Node Application Github Repo Link](https://github.com/DipakBodare/node-api-backend)  

## Local Demo of Node App

## Install nodejs on EC2 using PPA (Personal Package Archive).
- Pre-requisites: 
  - Should have ```non-root`` user account with ```sudo previledge```
  
- Download the Installation script
  ```
  cd ~
  curl -sL https://deb.nodesource.com/setup_16.x -o nodesource_sp.sh
  ```
  
- Run the Installation script with sudo previledge
  ```
  sudo bash nodesource_setup.sh
  ```
- Install the nodejs
  ```
  sudo apt install nodejs
  ```
  
- Check the Nodejs Version
  ```
  node -v
  ``` 
 
## Install PM2 on EC2 Instance
- PM2 Called as a ```Product Process Manager```
- PM2 is a free open source, advanced, efficient and cross-platform production-level process manager
- it also has incredible support for major Node.js frameworks such as Express, Adonis Js, Sails, Hapi and more, without need for any code changes.
- It has following features
  - App monitoring, 
  - Efficient management of micro-services/processes. 
  - Running apps in cluster mode. 
  - Graceful start and shutdown of apps.  
- Install the latest version of PM2
  ```
  sudo npm i -g pm2 
  ```
  
## Install Mongodb Database on EC2 Instance

## Clone the application git repository on EC2 Instance

## Configure Nginx File for Node App

## Acccess the Node app using IP address and Domain Name

## Create SSL Certificates for Nodejs App

