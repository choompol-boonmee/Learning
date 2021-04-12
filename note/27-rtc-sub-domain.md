
```
==========================================
domain sub1.thamdee.net 164.90.239.20
domain stun.sub1.thamdee.net 164.90.239.20
domain turn.sub1.thamdee.net 164.90.239.20

ssh -i key/id_rsa_do01 root@164.90.239.20
adduser choompol
chm
usermod -aG sudo choompol
rsync --archive --chown=choompol:choompol ~/.ssh /home/choompol

sudo vi /etc/ssh/sshd_config
Port 6060
service ssh restart
sudo ufw allow 6060
sudo ufw enable
sudo ufw status

===== in new terminal
ssh -p 6060 -i key/id_rsa_do01 choompol@sub1.thamdee.net

======================== BUILD WEB
=== https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04

sudo apt update
sudo apt install -y nginx
sudo ufw app list
sudo ufw allow 'Nginx HTTP'
sudo ufw status
systemctl status nginx

ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'
curl -4 sub1.thamdee.net

http://sub1.thamdee.net

sudo mkdir -p /var/www/sub1.thamdee.net/html
sudo chown -R $USER:$USER /var/www/sub1.thamdee.net/html
sudo chmod -R 755 /var/www/sub1.thamdee.net
vi /var/www/sub1.thamdee.net/html/index.html
<html><h1>HELLO</h1></html>

sudo vi /etc/nginx/sites-available/sub1.thamdee.net
server {
        listen 80;
        listen [::]:80;
        root /var/www/sub1.thamdee.net/html;
        index index.html index.htm index.nginx-debian.html;
        server_name sub1.thamdee.net www.sub1.thamdee.net;
        location / {
                try_files $uri $uri/ =404;
        }
}

sudo ln -s /etc/nginx/sites-available/sub1.thamdee.net /etc/nginx/sites-enabled/
sudo vi /etc/nginx/nginx.conf
http {
    ...
    server_names_hash_bucket_size 64;
    ...
}

sudo nginx -t
sudo systemctl restart nginx
sudo systemctl reload nginx

http://sub1.thamdee.net

======================== BUILD SECURE
https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04

sudo add-apt-repository ppa:certbot/certbot

sudo apt install -y python-certbot-nginx


sudo ufw status
sudo ufw allow 'Nginx Full'
sudo ufw delete allow 'Nginx HTTP'
sudo ufw status

sudo certbot --nginx -d sub1.thamdee.net -d www.sub1.thamdee.net -d turn.sub1.thamdee.net -d stun.sub1.thamdee.net

/etc/letsencrypt/live/sub1.thamdee.net/fullchain.pem
/etc/letsencrypt/live/sub1.thamdee.net/privkey.pem
/etc/letsencrypt
sudo certbot renew --dry-run
==============================================
sudo letsencrypt certonly --standalone -d sub1.thamdee.net -d stun.sub1.thamdee.net -d turn.sub1.thamdee.net
sudo letsencrypt renew

==============================================
curl -sL https://deb.nodesource.com/setup_8.x -o nodesource_setup.sh
vi nodesource_setup.sh
sudo bash nodesource_setup.sh

sudo apt-get install -y nodejs
sudo apt-get install -y gcc g++ make
curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn

nodejs -v
npm -v
sudo apt install -y build-essential
cd ~
vi hello.js
>>>>>
const http = require('http');

const hostname = 'localhost';
const port = 3000;
const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World!\n');
});
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
<<<<<

node hello.js
curl http://localhost:3000

sudo npm install pm2@latest -g
pm2 start hello.js
pm2 startup systemd

sudo env PATH=$PATH:/usr/bin /usr/lib/node_modules/pm2/bin/pm2 startup systemd -u choompol --hp /home/choompol

pm2 save

sudo systemctl start pm2-choompol
systemctl status pm2-choompol

pm2 stop hello
pm2 restart hello
pm2 list
pm2 info hello
pm2 monit

sudo vi /etc/nginx/sites-available/sub1.thamdee.net
>>>>>
    location /prj05 {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
<<<<<
sudo nginx -t
sudo systemctl restart nginx

==============================================
sudo apt-get install -y coturn
systemctl stop coturn

sudo vi /etc/default/coturn
TURNSERVER_ENABLED=1

sudo mv /etc/turnserver.conf /etc/turnserver.conf.original
sudo vi /etc/turnserver.conf
>>>>>>>
# /etc/turnserver.conf
listening-port=3478
tls-listening-port=5349
fingerprint
lt-cred-mech
server-name=sub1.thamdee.net
realm=sub1.thamdee.net
user=guest:somepassword
total-quota=100
stale-nonce=600
cert=/etc/letsencrypt/live/sub1.thamdee.net/cert.pem
pkey=/etc/letsencrypt/live/sub1.thamdee.net/privkey.pem
cipher-list="ECDHE-RSA-AES256-GCM-SHA512:DHE-RSA-AES256-GCM-SHA512:ECDHE-RSA-AES256-GCM-SHA384:DHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384"
proc-user=turnserver
proc-group=turnserver
<<<<<<<

sudo ufw allow 3478
sudo ufw allow 5349
systemctl start coturn
systemctl status coturn

https://webrtc.github.io/samples/src/content/peerconnection/trickle-ice/

sudo turnadmin -a -u choompol -r sub1.thamdee.net -p Choompol8086

stun:stun.sub1.thamdee.net:3478
turn:turn.sub1.thamdee.net:3478
stun:stun.sub1.thamdee.net:5349
turn:turn.sub1.thamdee.net:5349

```
