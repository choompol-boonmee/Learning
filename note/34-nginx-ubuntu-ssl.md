```


sudo apt-get install -y nginx
sudo apt-get install -y nginx

sudo systemctl status nginx

export HOST=node01.popiang.com

ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'
curl -4 $HOST

sudo mkdir -p /var/www/$HOST/html
sudo chown -R $USER:$USER /var/www/$HOST/html
sudo chmod -R 755 /var/www/$HOST
vi /var/www/$HOST/html/index.html
<html><h1>HELLO</h1></html>

sudo vi /etc/nginx/sites-available/$HOST
server {
        listen 80;
        listen [::]:80;
        root /var/www/node01.popiang.com/html;
        server_name node01.popiang.com;
        index index.html index.htm index.nginx-debian.html;
        location / {
                try_files $uri $uri/ =404;
        }
}

sudo ln -s /etc/nginx/sites-available/$HOST /etc/nginx/sites-enabled/
sudo vi /etc/nginx/nginx.conf
http {
    ...
    server_names_hash_bucket_size 64;
    ...
}

sudo nginx -t
sudo systemctl restart nginx
sudo systemctl reload nginx

http://node01.popiang.com

sudo apt install -y python3-certbot-nginx

sudo certbot --nginx -d $HOST
>>>>
sudo certbot renew --dry-run
sudo letsencrypt renew

sudo nginx -t
sudo systemctl restart nginx
https://node03.popiang.com

```

