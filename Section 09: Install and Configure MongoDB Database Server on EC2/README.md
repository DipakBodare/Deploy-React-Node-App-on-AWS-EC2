# <h1 align="center"> Install and configure MongoDB on EC2 Instance </h1>

<img align="center" src="https://github.com/DipakBodare/udemy-course-images/blob/main/ec2/nginx.png" height="100" alt="Nginx"> 

- [Official Link](https://www.mongodb.com/)

## What is MongoDB?
- MongoDB is a source-available cross-platform document-oriented database program.
- MongoDB is a object-oriented, straightforward, and flexible NoSQL database.
- It stores data in documents that resemble JSON. 
- 

## Installation of MongoDB
- Install the System Updates
  ```
  sudo apt update
  sudo apt install wget curl gnupg2 software-properties-common apt-transport-https ca-certificates lsb-release
  ```
- Import the public key
  ```
  curl -fsSL https://www.mongodb.org/static/pgp/server-6.0.asc|sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/mongodb-6.gpg
  ```
- Configure MongoDB Repo
  ```
  echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu $(lsb_release -cs)/mongodb-org/6.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-6.0.list
  ``` 
- Install MongoDB 6.0 on Ubuntu 22.04
  ```
  wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb
  sudo dpkg -i ./libssl1.1_1.1.1f-1ubuntu2.16_amd64.deb
  sudo apt update
  sudo apt install mongodb-org
  ```
- Start and enable MongoDB
  ```
  sudo systemctl enable --now mongod
  ```
- Check MongoDB Status
  ```
  systemctl status mongod
  ```
  - Output should be look like this
    ```
    mongod.service - MongoDB Database Server
     Loaded: loaded (/lib/systemd/system/mongod.service; enabled; vendor preset: enabled)
     Active: active (running) since Fri 2023-01-30 05:10:46 EAT; 8s ago
       Docs: https://docs.mongodb.org/manual
     Main PID: 436451 (mongod)
       Memory: 66.6M
       CGroup: /system.slice/mongod.service
               └─430451 /usr/bin/mongod --config /etc/mongod.conf
    Jan 30 05:10:46 dipak-PC systemd[1]: Started MongoDB Database Server.
    ```
- Check MongoDB Version
  ```
  mongod --version
  ```
  
## Configuration of MongoDB 6.0 on Ubuntu 22.04
- The configuration file for MongoDB is located at `/etc/mongod.conf`
- Enable Password Authentication
  - Open the Config file  
    ```
    sudo vim /etc/mongod.conf
    ```
  - Find and Uncomment the following Line
    ```
    security:
      authorization: enabled
    ```  
- Enable Remote Access on MongoDB 6.0
  - MongoDB is typically configured to only allow local access.
  - You must modify the code below to include the server IP or hostname as preferred if you want to access it remotely.
  ```
  # network interfaces
  net:
    port: 27017
    bindIp: 127.0.0.1  # Enter 0.0.0.0,:: to bind to all IPv4 and IPv6 addresses or, alternatively, use the net.bindIpAll setting.
  ```
  
## MongoDB Management Command
| Sr No | Command Uses | Command |
|-------|--------------|---------|
| 1 | To start the mongoDB | `sudo systemctl start mongod` |
| 2 | To restart the mongoDB | `sudo systemctl restart mongod` |
| 3 | To stop the MongoDB | `sudo systemctl stop mongod` |
| 4 | To enable auto-start after system reboot | `sudo systemctl enable mongod` |
  
  
