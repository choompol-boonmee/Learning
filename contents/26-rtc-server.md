```
==========================================
ssh -i key/id_rsa_do01 root@68.183.77.154
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
ssh -p 6060 -i key/id_rsa_do01 choompol@thaisdg.com

======================== BUILD WEB
=== https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-18-04

sudo apt update
sudo apt install -y nginx
sudo ufw app list
sudo ufw allow 'Nginx HTTP'
sudo ufw status
systemctl status nginx

ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'
curl -4 thaisdg.com

http://thaisdg.com

sudo mkdir -p /var/www/thaisdg.com/html
sudo chown -R $USER:$USER /var/www/thaisdg.com/html
sudo chmod -R 755 /var/www/thaisdg.com
vi /var/www/thaisdg.com/html/index.html
<html><h1>HELLO</h1></html>

sudo vi /etc/nginx/sites-available/thaisdg.com
server {
        listen 80;
        listen [::]:80;
        root /var/www/thaisdg.com/html;
        index index.html index.htm index.nginx-debian.html;
        server_name thaisdg.com www.thaisdg.com;
        location / {
                try_files $uri $uri/ =404;
        }
}

sudo ln -s /etc/nginx/sites-available/thaisdg.com /etc/nginx/sites-enabled/
sudo vi /etc/nginx/nginx.conf
http {
    ...
    server_names_hash_bucket_size 64;
    ...
}

sudo nginx -t
sudo systemctl restart nginx

http://thaisdg.com

======================== BUILD SECURE
https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-with-let-s-encrypt-on-ubuntu-18-04

sudo add-apt-repository ppa:certbot/certbot
sudo apt install -y python-certbot-nginx

sudo vi /etc/nginx/sites-available/thaisdg.com
server_name thaisdg.com www.thaisdg.com;

sudo nginx -t
sudo systemctl reload nginx

sudo ufw status
sudo ufw allow 'Nginx Full'
sudo ufw delete allow 'Nginx HTTP'
sudo ufw status

sudo certbot --nginx -d thaisdg.com -d www.thaisdg.com -d turn.thaisdg.com -d stun.thaisdg.com

/etc/letsencrypt/live/thaisdg.com/fullchain.pem
/etc/letsencrypt/live/thaisdg.com/privkey.pem
/etc/letsencrypt
sudo certbot renew --dry-run
==============================================
sudo letsencrypt certonly --standalone -d thaisdg.com -d www.thaisdg.com -d stun.thaisdg.com -d turn.thaisdg.com
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

sudo vi /etc/nginx/sites-available/thaisdg.com
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
server-name=thaisdg.com
realm=thaisdg.com
user=guest:somepassword
total-quota=100
stale-nonce=600
cert=/etc/letsencrypt/live/thaisdg.com/cert.pem
pkey=/etc/letsencrypt/live/thaisdg.com/privkey.pem
cipher-list="ECDHE-RSA-AES256-GCM-SHA512:DHE-RSA-AES256-GCM-SHA512:ECDHE-RSA-AES256-GCM-SHA384:DHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384"
proc-user=turnserver
proc-group=turnserver
<<<<<<<

sudo ufw allow 3478
sudo ufw allow 5349
systemctl start coturn
systemctl status coturn

sudo turnadmin -a -u choompol -r thaisdg.com -p Choompol8086

stun:stun.thaisdg.com:3478
turn:turn.thaisdg.com:3478
stun:stun.thaisdg.com:5349
turn:turn.thaisdg.com:5349

test at
https://webrtc.github.io/samples/src/content/peerconnection/trickle-ice/

```
