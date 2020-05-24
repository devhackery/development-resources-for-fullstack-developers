# Any application runs on particular port

> Steps to deploy a React/Node.js app using PM2, NGINX as a reverse proxy and an SSL from LetsEncrypt multiple application runnig in diffrent port



## 1. Login via ssh
 I will be using the root user, but would suggest creating a new user.

## 2. configure DNS for your domain name 
Go to your doamin provider site 



1. Log in to your Account Manager.
2. Next to Domains, click Manage.
3. Select the domain name you want to use, click Settings and select Manage DNS. Click the Settings tab.
4. Under Nameservers, click Manage.
5. Under Setup type, A Record (add you server public IP)


## 3. Findout port
Findout your applications runnig ports

eg: 5000

## 4. Install NGINX and configure
```
sudo apt install nginx
```


## 5. NGINX  revese proxy configuration

```
cd /etc/nginx/sites-available
sudo scp /etc/nginx/sites-available/default yourdomain.com
sudo nano /etc/nginx/sites-available/yourdomain.com
```

You can edit default configuration that directly poin to port 80 ,But I recoment not to edit default trust me on this 


Add the following to the location part of the server block
```
    server_name yourdomain.com www.yourdomain.com;

    location / {
        proxy_pass http://localhost:5000; #whatever port your app runs on
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
```


## 6. Enable your Server Blocks and Restart Nginx

Now that we have our server block files, we need to enable them. We can do this by creating symbolic links from these files to the sites-enabled directory, which Nginx reads from during startup.

```
sudo ln -s /etc/nginx/sites-available/yourdomain.com /etc/nginx/sites-enabled/
```

Next, test to make sure that there are no syntax errors in any of your Nginx files:

```
# Check NGINX config
sudo nginx -t

# Restart NGINX
sudo service nginx restart
```



## 7. Add SSL with LetsEncrypt
```
sudo add-apt-repository ppa:certbot/certbot
sudo apt-get update
sudo apt-get install python-certbot-nginx
sudo certbot --nginx -d yourdomain.com -d www.yourdomain.com

# Only valid for 90 days, test the renewal process with
certbot renew --dry-run
```

Now visit https://yourdomain.com and you should see your app