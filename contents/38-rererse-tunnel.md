‘‘‘
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

===========================================
cd ~/Documents/wk21/do01

ssh num@192.168.2.203

ssh-keygen -t rsa -C "nuke03@d.edipa.org" -f nuke03-key
exit

sftp num@192.168.2.203
get nuke03-key.pub
bye

sftp -i key/id_rsa_do01 num@d.edipa.org
put nuke03-key.pub
bye

ssh -i key/id_rsa_do01 num@d.edipa.org
sudo adduser nuke03
... nuke03
sudo mkdir /home/nuke03/.ssh
sudo mv nuke03-key.pub /home/nuke03/.ssh/authorized_keys
sudo chown -R nuke03:nuke03 /home/nuke03/.ssh
exit

ssh num@192.168.2.203
ssh -i /home/num/nuke03-key nuke03@d.edipa.org
exit

sudo apt-get install -y autossh

ssh -R 8015:localhost:22 -i /home/num/nuke03-key nuke03@d.edipa.org

>>>> testing in other terminal
ssh -p 8015 num@d.edipa.org
exit
>>>> get back
exit

sudo vi /etc/systemd/system/edipa-nuke03-8015.service
>>>>>>
[Unit]
Description=AutoSSH tunnel service everythingcli MySQL on local port 5000
After=network.target
[Service]
Environment="AUTOSSH_GATETIME=0"
ExecStart=/usr/bin/autossh -M 0 -o "PubkeyAuthentication=yes" -o "PasswordAuthentication=no" -o "ServerAliveInterval=30" -o "ServerAliveCountMax=3" -NR 8015:localhost:22 -i /home/num/nuke03-key nuke03@d.edipa.org
User=num
[Install]
WantedBy=multi-user.target
<<<<<<

sudo systemctl daemon-reload
sudo systemctl enable edipa-nuke03-8015
sudo systemctl start edipa-nuke03-8015
sudo systemctl status edipa-nuke03-8015

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
‘‘‘
