<h1 align="center"> Deploy React App on AWS EC2 instance <h1>

## App Demo of React app

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
## Added `.env` file in `.gitignore`
- Not Push environment variable file in Online Git repo because all environment variables are in this file.
- You have to add manually on a server while builing the application manually

## Deploy the application on EC2 Instance
- Install the git on EC2 instance
  ```
  sudo apt update
  sudo apt install git
  ```
   
- Check the git verison
  ```
  git --version
  ```
- Create the directory for applications
  ```
  sudo mkdir -p /var/www/domain_name  
  ```	
	
- Assign user permissions for directory	
  ```
  sudo chown -R $USER:$USER /var/www/domain_name/
  ```
- Allow the permissions only to owner to ```read```, ```write```, and ```execute``` the files   
  ```
  sudo chmod -R 755 /var/www/domain_name
  ```
- Clone the git repo
  ```
  git clone git@github.com:DipakBodare/react-app-frontend.git
  ```  
	
## Configure Nginx File for React App
- Create the nginx config file
  ```
  sudo touch /etc/nginx/sites-available/domain_name
  ```
  
- Add the below content in nginx config file  
  
  - Open the nginx file and add the below nginx config file
    ```
    sudo vim /etc/nginx/sites-available/domain_name
    ```
    
    ```
    server {
	  listen 80;
          server_name <font color="red">your_domain_name!</font>;

		root /var/www/domain_name/react-app-frontend/build;
		try_files $uri $uri/ /index.html =404;
          client_max_body_size 50M;
          
          location ~ /.well-known {
                  allow all;
          }

		#location / {
	        #	root /var/www/domain_name/react-app-frontend/build;
	        #	try_files $uri $uri/ /index.html =404;
	        #}
	
	        #location / {
                # First attempt to serve request as file, then
                # as directory, then fall back to displaying a 404.
 	        #add_header 'Access-Control-Allow-Origin' '*';
                #add_header 'Access-Control-Allow-Methods' 'GET, POST, OPTIONS';
		#add_header 'Access-Control-Allow-Headers' 'Origin, X-Requested-With, Content-Type, Accept';
        	#proxy_pass http://127.0.0.1:3035;
                #proxy_read_timeout 3600;
                #proxy_connect_timeout 3600;
                #proxy_send_timeout 3600;
                #proxy_read_timeout 3600;
                #send_timeout 3600;  
                #try_files $uri $uri/ /index.html =404;
          #}

    }
    ```
  
- Create the symbolic link for site
  ```
  sudo ln -s /etc/nginx/sites-available/domain_name /etc/nginx/sites-enabled/
  ```
  
- Validate the nginx config file
  ```
  nginx -t
  ```
  
- Restart the nginx service
  ```
  sudo service nginx restart
  ```
    
## Access the React app using Doamin Name  
```
http://your_server_ip
```
	

