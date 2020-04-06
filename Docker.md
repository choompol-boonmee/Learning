==========================
adduser choompol
usermod -aG sudo choompol
su choompol
mkdir .ssh
exit
cp ~/.ssh/authorized_keys /home/choompol/.ssh/.
chown choompol /home/choompol/authorized_keys
chgrp choompol /home/choompol/authorized_keys
su choompol
service ssh restart
sudo vi /etc/ssh/sshd_config
Port 6060
service ssh restart
cd /etc/update-motd.d/
sudo rm 10-help-text
sudo vi 50-landscape-sysinfo
/usr/bin/landscape-sysinfo --exclude-sysinfo-plugins=LandscapeLink
cd /etc/nginx/sites-enabled/
sudo add-apt-repository ppa:nginx/stable
sudo apt-get update
sudo apt-get install -y nginx
/etc/nginx/nginx.conf
cd /etc/nginx/sites-enabled
ln -s ../sites-available/new_file .
sudo service nginx restart

sudo ufw allow 6060
sudo ufw allow 80
sudo ufw enable
sudo ufw status

sudo apt update
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
sudo apt update
sudo apt upgrade -y
apt-cache policy docker-ce
sudo apt install -y docker-ce
sudo systemctl status docker
sudo usermod -aG docker ${USER}
id -nG
su - ${USER}
id -nG
docker
docker info
docker run hello-world
docker search ubuntu
docker images
docker login -u choompol
docker run --rm -i -t ubuntu:precise /bin/bash
docker ps -a
docker images
pstree
sudo apt-get install git git-core
sudo useradd -m -U -r -s /bin/bash git
chmod a+r /tmp/id_rsa.pub
sudo apt-get install -y gitolite3

apt-cache search gitolite

sudo su git
cd
gitolite setup -pk xxx.pub

ssh-keygen
ssh-keygen -f choompol_id_rsa
scp ~/.ssh/id_rsa.pub beatum1:/tmp/
vi ~/.ssh/config
>>>>>>>>>>>>>>>>
Host beatum0
    HostName 128.199.143.165
    Port 6060
    IdentityFile ~/.ssh/id_rsa
    User root

Host beatum1
    HostName 128.199.143.165
    Port 6060
    IdentityFile ~/.ssh/choompol_id_rsa
    User choompol
<<<<<<<<<<<<<<<<<<<

mkdir -p /var/www
sudo chown -R www-data:www-data /var/www
sudo chmod +s /var/www
sudo mkdir /var/www/blog

sudo rm /etc/nginx/sites-enabled/default
sudo vi /etc/nginx/sites-available/blog
>>>>>>>>>>>>>
<<<<<<<<<<<<<
cd /etc/nginx/sites-enabled
sudo ln -s ../sites-available/blog
sudo service nginx reload

apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 36A1D7869245C8950F966E92D8576A8BA88D21E9
echo deb http://get.docker.io/ubuntu docker main> /etc/apt/sources.list.d/docker.list
apt-get update
apt-get install lxc-docker

===== gitolite3
dpkg-reconfigure gitolite3
https://askubuntu.com/questions/853140/how-do-i-configure-gitolite3-to-use-the-git-account-on-ubuntu-lts-16
https://serverfault.com/questions/528491/replace-gitolite3-user-with-git

