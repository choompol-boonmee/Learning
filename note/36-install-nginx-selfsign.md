```
========================== SELF SIGNED NGINX1 BEGIN
sudo apt-get install -y nginx
curl -4 localhost
...
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt

sudo openssl dhparam -out /etc/ssl/certs/dhparam.pem 2048
sudo nano /etc/nginx/snippets/self-signed.conf
>>>>>>
ssl_certificate /etc/ssl/certs/nginx-selfsigned.crt;
ssl_certificate_key /etc/ssl/private/nginx-selfsigned.key;
<<<<<<
sudo nano /etc/nginx/snippets/ssl-params.conf
>>>>>>
# from https://cipherli.st/
# and https://raymii.org/s/tutorials/Strong_SSL_Security_On_nginx.html
ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
ssl_prefer_server_ciphers on;
ssl_ciphers "EECDH+AESGCM:EDH+AESGCM:AES256+EECDH:AES256+EDH";
ssl_ecdh_curve secp384r1;
ssl_session_cache shared:SSL:10m;
ssl_session_tickets off;
ssl_stapling on;
ssl_stapling_verify on;
resolver 8.8.8.8 8.8.4.4 valid=300s;
resolver_timeout 5s;
# Disable preloading HSTS for now.  You can use the commented out header line that includes
# the "preload" directive if you understand the implications.
#add_header Strict-Transport-Security "max-age=63072000; includeSubdomains; preload";
add_header Strict-Transport-Security "max-age=63072000; includeSubdomains";
add_header X-Frame-Options DENY;
add_header X-Content-Type-Options nosniff;
ssl_dhparam /etc/ssl/certs/dhparam.pem;
<<<<<<

sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/default.bak
sudo nano /etc/nginx/sites-available/default
>>>>>>
...
        listen 443 ssl;
        listen [::]:443 ssl;
        include snippets/self-signed.conf;
        include snippets/ssl-params.conf;
...
<<<<<<
sudo nginx -t
sudo systemctl restart nginx
========================== SELF SIGNED NGINX1 END

========================== SELF SIGNED NGINX2 BEGIN
sudo apt-get install -y nginx
curl -4 localhost
...
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/nginx-selfsigned.key -out /etc/ssl/certs/nginx-selfsigned.crt

sudo openssl dhparam -out /etc/nginx/dhparam.pem 4096
sudo mkdir /etc/nginx/snippets
sudo nano /etc/nginx/snippets/self-signed.conf
>>>>>>
ssl_certificate /etc/ssl/certs/nginx-selfsigned.crt;
ssl_certificate_key /etc/ssl/private/nginx-selfsigned.key;
<<<<<<
sudo nano /etc/nginx/snippets/ssl-params.conf
>>>>>>
ssl_protocols TLSv1.2;
ssl_prefer_server_ciphers on;
ssl_dhparam /etc/nginx/dhparam.pem;
ssl_ciphers ECDHE-RSA-AES256-GCM-SHA512:DHE-RSA-AES256-GCM-SHA512:ECDHE-RSA-AES256-GCM-SHA384:DHE-RSA-AES25>
ssl_ecdh_curve secp384r1; # Requires nginx >= 1.1.0
ssl_session_timeout  10m;
ssl_session_cache shared:SSL:10m;
ssl_session_tickets off; # Requires nginx >= 1.5.9
ssl_stapling on; # Requires nginx >= 1.3.7
ssl_stapling_verify on; # Requires nginx => 1.3.7
resolver 8.8.8.8 8.8.4.4 valid=300s;
resolver_timeout 5s;
# Disable strict transport security for now. You can uncomment the following
# line if you understand the implications.
# add_header Strict-Transport-Security "max-age=63072000; includeSubDomains; preload";
add_header X-Frame-Options DENY;
add_header X-Content-Type-Options nosniff;
add_header X-XSS-Protection "1; mode=block";
<<<<<<

sudo cp /etc/nginx/sites-available/default /etc/nginx/sites-available/default.bak
sudo nano /etc/nginx/sites-available/default
>>>>>>
...
        listen 443 ssl;
        listen [::]:443 ssl;
        include snippets/self-signed.conf;
        include snippets/ssl-params.conf;
...
<<<<<<
sudo nginx -t
sudo systemctl restart nginx
========================== SELF SIGNED NGINX2 END

========================== SELF SIGNED NGINX3 BEGIN
sudo apt-get install -y nginx
curl -4 localhost
sudo nano localhost.conf
>>>>>>
[req]
default_bits       = 2048
default_keyfile    = localhost.key
distinguished_name = req_distinguished_name
req_extensions     = req_ext
x509_extensions    = v3_ca
[req_distinguished_name]
countryName                 = Country Name (2 letter code)
countryName_default         = TH
stateOrProvinceName         = State or Province Name (full name)
stateOrProvinceName_default = Bangkok
localityName                = Locality Name (eg, city)
localityName_default        = Donmuang
organizationName            = Organization Name (eg, company)
organizationName_default    = localhost
organizationalUnitName      = organizationalunit
organizationalUnitName_default = Development
commonName                  = Common Name (e.g. server FQDN or YOUR name)
commonName_default          = 192.168.2.203
commonName_max              = 64
[req_ext]
subjectAltName = @alt_names
<<<<<<
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout localhost.key -out localhost.crt -config localhost.conf
sudo cp localhost.crt /etc/ssl/certs/localhost.crt
sudo cp localhost.key /etc/ssl/private/localhost.key
sudo nano /etc/nginx/sites-available/default
>>>>>>
        listen 443 ssl http2;
        listen [::]:443 ssl http2;
        ssl_certificate /etc/ssl/certs/localhost.crt;
        ssl_certificate_key /etc/ssl/private/localhost.key;
        ssl_protocols TLSv1.2 TLSv1.1 TLSv1;
<<<<<<
sudo nginx -t
sudo systemctl restart nginx
========================== SELF SIGNED NGINX3 END

========================== SELF SIGNED NGINX4 BEGIN
sudo apt-get install -y nginx
curl -4 localhost
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/ssl/private/localhost.key -out /etc/ssl/certs/localhost.crt

sudo nano /etc/nginx/sites-available/default
>>>>>>
        listen 443 ssl http2;
        listen [::]:443 ssl http2;
        ssl_certificate /etc/ssl/certs/localhost.crt;
        ssl_certificate_key /etc/ssl/private/localhost.key;
        ssl_protocols TLSv1.2 TLSv1.1 TLSv1;
<<<<<<
sudo nginx -t
sudo systemctl restart nginx
========================== SELF SIGNED NGINX3 END

```
