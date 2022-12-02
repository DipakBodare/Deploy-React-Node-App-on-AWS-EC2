# Install Node.js on ubuntu server

Step 1: Update the sercer
```
sudo apt update
```

Step 2: install node.js with "apt" utility on ubuntu server
```
sudo apt install nodejs
```
# Install Specific nodejs verison on ubuntu instance
Step 1: Add PPA repository in ubuntu. we are going to install nodejs 18.xx version in this section.
```
curl -sL https://deb.nodesource.com/setup_18.x -o nodesource_setup.sh
```
Step 2: Run the Shell script that you have downdloaded in the above steps
```
sudo bash nodesource_setup.sh
```
Step 3: Run the nodejs install command
```
sudo apt install nodejs
```
Step 4: Check the Nodejs version
```
node -v
```
# Install NPM (Node process manager)
```
sudo apt install npm
```

# install PM2 on EC2 instance
```
sudo npm install pm2@latest -g
```
- To automatically run the pm2 process when server reboot or shutdown
```
pm2 startup systemd
```
- Output should be like this
```
Output
[PM2] Init System found: systemd
sammy
[PM2] To setup the Startup Script, copy/paste the following command:
sudo env PATH=$PATH:/usr/bin /usr/lib/node_modules/pm2/bin/pm2 startup systemd -u sumit --hp /home/sumit
```
- Run command from the above output 
  ```
  sudo env PATH=$PATH:/usr/bin /usr/lib/node_modules/pm2/bin/pm2 startup systemd -u sumit --hp /home/sumit
  ```
- To save the PM2 process list and corresponding environments:
  ```
  pm2 save
  ```



