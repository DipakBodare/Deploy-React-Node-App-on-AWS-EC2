# <h1 align=center> Deploy Node.js app on AWS EC2 instance <h1>

## What is Node.js?
- Node.js is a JavaScript runtime for server-side programming. 
- we can create scalable backend functionality using JavaScript  
  
## [Node Application Github Repo Link](https://github.com/DipakBodare/node-api-backend)  

## Install nodejs on EC2 using PPA (Personal Package Archive).
- Pre-requisites: 
  - Should have ```non-root``` user account with ```sudo previledge```
  
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
## PM2 Management Commands
### Common Process command  
   
  | Sr No | Command Uses | Command |
  |------|--------|---------|
  | 1 | To view details of a single Node process | `pm2 show 0` |
  | 2 | Stop all apps | `pm2 stop all` |  
  | 3 | Stop process with ID 0 | `pm2 stop 0` | 
  | 4 | Restart all apps | `pm2 restart all` |
  | 5 | Reset all counters | `pm2 reset 0` | 
  | 6 | Kill and remove all apps | `pm2 delete all` |
  | 7 | Kill and delete app with ID 0 | `pm2 delete 0` |
 
### To manage application logs  
  | Sr No | Command Uses | Command |
  |------|--------|---------|
  | 1 | View logs for all processes | `pm2 logs` |
  | 2 | View logs for app 0  | `pm2 logs 0` |
  | 3 | View logs for all processes in JSON format | `pm2 logs --json` |
  | 4 | Flush all logs | `pm2 flush` |
 
### To manage the PM2 process
  | Sr No | Command Uses | Command |
  |------|--------|---------|
  | 1 | Enable PM2 to start at system boot | `pm2 startup` |
  | 2 | Explicitly specify systemd as startup system | `pm2 startup systemd` |
  | 3 | Save current process list on reboot | `pm2 save` |
  | 4 | Disable PM2 from starting at system boot | `pm2 unstartup` |
  | 5 | Update PM2 package | `pm2 update` | 
  
## Install Mongodb Database on EC2 Instance

## Clone the application git repository on EC2 Instance

## Configure Nginx File for Node App

## Acccess the Node app using IP address and Domain Name

## Create SSL Certificates for Nodejs App

