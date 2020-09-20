```
===========================================
===========================================
===========================================
1.nuke01	num@192.168.2.201	8013
2.nuke02	num@192.168.2.202	8014
3.nuke03	num@192.168.2.203	8015
4.bmf01		num@192.168.2.204	8004
5.rpi4b01	num@192.168.2.158	8005
6.rpi4b02	num@192.168.2.176	8006
7.rpi4b03	num@192.168.2.172	8007
8.rpi4b04	num@192.168.2.127	8008
9.opiz01	num@192.168.2.144	8009
10.dell01	num@192.168.2.137	8010
11.hp01		num@192.168.2.111	8011
12.bmfwin01	192.168.2.195:3389	8012
13.rock01   num@192.168.2.150 8016

===========================================
cd ~/Documents/wk21/do01

ssh num@192.168.2.150

ssh-keygen -t rsa -C "rock01@d.edipa.org" -f rock01-key
exit

sftp num@192.168.2.150
get rock01-key.pub
bye

sftp -i key/id_rsa_do01 num@d.edipa.org
put rock01-key.pub
bye

ssh -i key/id_rsa_do01 num@d.edipa.org
sudo adduser rock01
... rock01
sudo mkdir /home/rock01/.ssh
sudo mv rock01-key.pub /home/rock01/.ssh/authorized_keys
sudo chown -R rock01:rock01 /home/rock01/.ssh
exit

ssh num@192.168.2.150
ssh -i /home/num/rock01-key rock01@d.edipa.org
exit

sudo apt-get install -y autossh

ssh -R 8016:localhost:22 -i /home/num/rock01-key rock01@d.edipa.org

>>>> testing in other terminal
ssh -p 8016 num@d.edipa.org
exit
>>>> get back
exit

sudo vi /etc/systemd/system/edipa-rock01-8016.service
>>>>>>
[Unit]
Description=AutoSSH tunnel service everythingcli MySQL on local port 5000
After=network.target
[Service]
Environment="AUTOSSH_GATETIME=0"
ExecStart=/usr/bin/autossh -M 0 -o "PubkeyAuthentication=yes" -o "PasswordAuthentication=no" -o "ServerAliveInterval=30" -o "ServerAliveCountMax=3" -NR 8016:localhost:22 -i /home/num/rock01-key rock01@d.edipa.org
User=num
[Install]
WantedBy=multi-user.target
<<<<<<

sudo systemctl daemon-reload
sudo systemctl enable edipa-rock01-8016
sudo systemctl start edipa-rock01-8016
sudo systemctl status edipa-rock01-8016

exit


===========================================
ssh num@192.168.2.203
ssh -R 8012:192.168.2.195:3389 -i /home/num/nuke03-key nuke03@d.edipa.org

>>>> test remote desktop

exit

sudo vi /etc/systemd/system/edipa-bmfwin01-8012.service
>>>>>>
[Unit]
Description=AutoSSH tunnel service everythingcli MySQL on local port 5000
After=network.target
[Service]
Environment="AUTOSSH_GATETIME=0"
ExecStart=/usr/bin/autossh -M 0 -o "PubkeyAuthentication=yes" -o "PasswordAuthentication=no" -o "ServerAliveInterval=30" -o "ServerAliveCountMax=3" -NR 8012:192.168.2.195:3389 -i /home/num/nuke03-key nuke03@d.edipa.org
User=num
[Install]
WantedBy=multi-user.target
<<<<<<

sudo systemctl daemon-reload
sudo systemctl enable edipa-bmfwin01-8012
sudo systemctl start edipa-bmfwin01-8012
sudo systemctl status edipa-bmfwin01-8012

exit

===========================================
===========================================
```
