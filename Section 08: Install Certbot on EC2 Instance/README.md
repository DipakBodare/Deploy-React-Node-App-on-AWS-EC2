## Install Certbot on EC2 Instance

## What is Letsencrypt?
- Let’s Encrypt is a Certificate Authority (CA) that provides an accessible way to obtain and install free TLS/SSL certificates

## Pre-requisites
- Need `sudo enabled` user or `root` access
- Need Registered Domain Name
- Nginx Should be installed on a server
- Domain mapped to Server IP address

### Note: This certbot installation is used for ```Ubuntu 22.04``` Distribution. Might be this command will not work on other Distribution.


## Install Letsencrypt on EC2 instance

- Install snap on a server
  ```
  sudo snap install core; sudo snap refresh core
  ```
  
- Install certbot package
  ```
  sudo snap install --classic certbot
  ```
  
- Link Certbot command with snap so you can run the command from any location inside server
  ```
  sudo ln -s /snap/bin/certbot /usr/bin/certbot
  ```
   
## Create SSL Certificates for React App 
```
sudo certbot --nginx -d domain_name -d domain_name
```
## Verify Certbot Auto-renewal
- Let’s Encrypt’s certificates are only valid for ```90 days```.
- so need to enable systemd timer

- Verify the status of timer
```
sudo systemctl status snap.certbot.renew.service
```

- Test the renewal process
```
sudo certbot renew --dry-run
```
