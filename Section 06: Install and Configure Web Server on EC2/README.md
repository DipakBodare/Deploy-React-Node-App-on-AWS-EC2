# <h1 align="center"> Introduction to Nginx web Server </h1>

<img align="center" src="https://github.com/DipakBodare/udemy-course-images/blob/main/ec2/nginx.png" height="100" alt="Nginx"> 

- [Official Link](https://www.nginx.com/)

## What is Nginx
- Nginx is a web server that can also be used as a 
  - reverse proxy, 
  - load balancer, 
  - mail proxy
  - HTTP cache. 
 
- responsible for hosting some of the largest and highest-traffic sites on the internet.
- It is a lightweight choice that can be used as either a web server or reverse proxy.
- 
## Installation of Nginx Web server
- Install Nginx on EC2 Instance
  ```
  sudo apt -y update
  sudo apt -y install nginx
  ```
- Check the Nginx Web Server
  ```
  sudo systemctl status nginx
  ```
  - Output should be look like this
    ```
    nginx.service - A high performance web server and a reverse proxy server
      Loaded: loaded (/lib/systemd/system/nginx.service; enabled; vendor preset: enabled)
      Active: active (running) since Fri 2022-03-01 16:08:19 UTC; 3 days ago
      Docs: man:nginx(8)
      Main PID: 2369 (nginx)
        Tasks: 2 (limit: 1153)
        Memory: 3.5M
        CGroup: /system.slice/nginx.service
               ├─2369 nginx: master process /usr/sbin/nginx -g daemon on; master_process on;
               └─2380 nginx: worker process
    ```
- Check the Nginx Main Page
  ```
  http://your)server_ip
  ```
## Managing the Nginx Process

- To stop the Web Server:
  ```
  sudo systemctl stop nginx
  ```
  
- To start the Web Server
  ```
  sudo systemctl start nginx
  ```
  
- To restart the Web server
  ```
  sudo systemctl restart nginx
  ```
  
- To reload the nginx config file without droping connections
  ```
  sudo systemctl reload nginx
  ```
  
- To start the nginx web server automatically when server reboots
  ```
  sudo systemctl enable nginx
  ```

- To start the nginx web server automatically when server reboots
  ```
  sudo systemctl disable nginx
  ```


