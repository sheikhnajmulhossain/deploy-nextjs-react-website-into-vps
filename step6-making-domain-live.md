# Making the domain live

1. navigate to your git project 
for example `cd yourproject`

2. Install nginx
`apt install nginx -y`

3. create a configuration file for the main domain  
`nano /etc/nginx/sites-available/yourdomainname.com`

4. paste this and change domain names

  server {

    listen 80;

    root /var/www/html;

    index index.html index.htm index.nginx-debian.html;

            server_name yourDomain.com www.yourDomain.com;

            location / {

                    proxy_pass http://localhost:3000;

                    proxy_http_version 1.1;

                    proxy_set_header Upgrade $http_upgrade;

                    proxy_set_header Connection 'upgrade';

                    proxy_set_header Host $host;

                    proxy_cache_bypass $http_upgrade;

                }

    }

5.  ctrl+o > enter > ctrl+x

6. Create a symbolic or soft link  
   `ln -s /etc/nginx/sites-available/yourdomain.com /etc/nginx/sites-enabled/yourdomain.com`

7. Check if the file content is right or not using test configuration.  
 `sudo nginx -t`

8.  Restart the nginx server  
   `sudo systemctl restart nginx`

9.  Install SSL through Certbot
`apt  install certbot`

10. generate SSL  
  `certbot`
