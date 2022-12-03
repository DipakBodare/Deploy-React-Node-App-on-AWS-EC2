# What is SSL
- SSL means secure socket layer
- Its a encryption based security protocol
- It ensures privacy, authentication and data ntegrity in Internet communications.

# How does SSL/TLS work
- SSL encrypts data that is transmitted across the web.
- anyone who tries to intercept this data will only see a garbled mix of characters that is nearly impossible to decrypt.
- SSL also digitally signs data in order to provide data integrity, verifying that the data is not tampered with before reaching its intended recipient.

# Why SSL/TLS is very important ?
- If a consumer visited a shopping website, placed an order, and entered their credit card number on the website, that credit card number would travel       across the Internet unconcealed.

temporary documentatio for ssl website for documentation
```
https://www.cloudflare.com/learning/ssl/what-is-ssl/
```
# Types of SSL certificate
- *Single Domain*: It applies to only one domain ( Name of website)
- *Wildcard*: it is also applies to only one domain but it applies multiple subdomain of same doamin name.
  for e.g test.abc.com, test2.abc.com
    where abc.com is the main domain and test, test1 is the subdomain
- *Multidomain*: SSL certicate can apply upto multiple unrelated domains


# Installation of SSL certificate

Pre-requisites:
- Need root access of server

- Step 1: Installing snap 
  ```
  sudo snap install core; sudo snap refresh core
  ```
- Step 2: Install classic certbot
  ```
  sudo snap install --classic certbot
  ```
- Step 3: link certbot commands to snap directoy
  ```
  sudo ln -s /snap/bin/certbot /usr/bin/certbot
  ```
      
        
