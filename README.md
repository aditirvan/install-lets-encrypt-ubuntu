# Let's Encrypt on Ubuntu
## Install
```
sudo apt install certbot python3-certbot-nginx
sudo nano /etc/nginx/sites-available/example.com
sudo nginx -t
sudo systemctl reload nginx
```
## Add to Nginx
```
sudo certbot --nginx -d example.com -d www.example.com
``` 
## check auto renewal
```
sudo systemctl status certbot.timer

#test renewal
sudo certbot renew --dry-run
```
## Restart Nginx
```
sudo nginx -t
sudo systemctl restart nginx
```
## Author
Adhithia Irvan Rachmawan <adhithia.irvan@gmail.com>
