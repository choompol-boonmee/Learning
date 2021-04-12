```
1. create none at digital ocean and get ip addr
2. set dns for the node, and stun/turn
3. login to the server
ssh -i key/id_rsa_do01 root@node04.popiang.com

adduser num
usermod -aG sudo num
rsync --archive --chown=num:num ~/.ssh /home/num
sudo vi /etc/ssh/sshd_config
service ssh restart
>>>> new terminal
ssh -p 6000 -i key/id_rsa_do01 num@node04.popiang.com

sudo apt-get update
sudo apt-get -y upgrade
sudo apt-get install -y net-tools
sudo lsof -i -P -n | grep LISTEN

