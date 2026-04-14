# NGINX Setup Guide for Ubuntu and Amazon Linux

This guide covers how to install and configure NGINX on both Ubuntu and Amazon Linux servers.

## Ubuntu Setup
### 1. Update system packages
    - sudo apt update && sudo apt upgrade -y
### 2. Install NGINX
    - sudo apt install nginx -y
### 3. Start NGINX service
    - sudo systemctl start nginx
### 4. Check NGINX status
    - sudo systemctl status nginx
### 5. Enable NGINX on boot
    - sudo systemctl enable nginx

#### Note:- Check your machine is not running on the given IP(copy and paste not redirect some time not workig)


## ☁️ Amazon Linux Setup
### 1. Update system packages
    - sudo dnf update -y
### 2. Install NGINX
    - sudo dnf install nginx -y
### 3. Start NGINX service
    - sudo systemctl start nginx
### 4. Enable NGINX on boot
    - sudo systemctl enable nginx
### 5. Check NGINX status
    - sudo systemctl status nginx
✅ Verify Installation


 ## Useful Commands
    Test NGINX config
          - sudo nginx -t
     Reload NGINX after config changes
         - sudo systemctl reload nginx
    Restart NGINX
        - sudo systemctl restart nginx

## NGINX Default Web Root and edit 
   ### Amazon Linux:
       - sudo cd /usr/share/nginx/html
       - nano index.html
       
   ## Ubuntu:
      - sudo cd /var/www/html
      - sudo nano index.nginx-debian.html
