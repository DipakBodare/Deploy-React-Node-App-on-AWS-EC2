# Install Node.js on ubuntu server

Step 1: Update the sercer
```
sudo apt update
```

Step 2: install node.js with "apt" utility on ubuntu server
```
sudo apt install nodejs
```
# Install Specifice nodejs verison on ubuntu instance
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






