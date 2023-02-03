<h1 align="center"> Introduction to React App <h1>

## Application Code
- [React application Github Repo Link](https://github.com/DipakBodare/react-app-frontend)  
  
## What is React.js
  - React is a free and open-source front-end JavaScript library for building user interfaces based on UI components.
  
# Shows Demo Locally
  
## How to build The react app  

- Install the applicaiton dependancies
  ```
  npm install
  ```
- Run the Application in Developement mode
  ```
  npm start
  ```
- Build the Application for production 
  ```
  npm run build
  ```
- Final Output
  - Final output is in `Build` folder
  
## Check the App Locally
- Copy Application in html folder and open the app
  ``` 
  cp -r /home/user/application_path/Build/ /var/www/html
  ```
- Open the application in a browser
  ```
  localhost
  ```
## Clone the application git repository
- Install the git on EC2 instance
  ```
  sudo apt update
  sudo apt install git
  ```
- Check the git verison
  ```
  git --version
 ``` 
- Clone the git repo
  ```
  git clone git@github.com:DipakBodare/react-app-frontend.git
  ```
- Copy the build folder in the ```html``` folder
  ```
  cp -r application_code/build/ /var/www/html/
  ```
- Access the app using IP address
  ``` 
  ip_adress_of_server
  ```
  
## Configure Nginx File for React App
- Create the nginx config file
  ```
  sudo touch /etc/nginx/sites-available/site-name
  ```
- Add the below content in nginx config file  
  - Open the nginx file
    ```
    sudo vim /etc/nginx/sites-available/site-name
    ```
  - Create the symbolic link for site
    ```
    sudo ln -s /etc/nginx/sites-available/site-name /etc/nginx/sites-enabled/
    ```
  - validate the nginx config file
    ```
    nginx -t
    ```
  - Restart the nginx service
    ```
    sudo service nginx restart
    ```
## Access the React app 

- 

