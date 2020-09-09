```


sudo apt-get install -y coturn
sudo systemctl stop coturn

sudo vi /etc/default/coturn
TURNSERVER_ENABLED=1

sudo mv /etc/turnserver.conf /etc/turnserver.conf.original
sudo vi /etc/turnserver.conf
>>>>>>>
# /etc/turnserver.conf
realm=turn05.popiang.com
user=guest:somepassword
listening-port=3478
fingerprint
lt-cred-mech
total-quota=100
stale-nonce=600
cipher-list="ECDHE-RSA-AES256-GCM-SHA512:DHE-RSA-AES256-GCM-SHA512:ECDHE-RSA-AES256-GCM-SHA384:DHE-RSA-AES256-GCM-SHA384:ECDHE-RSA-AES256-SHA384"
proc-user=turnserver
proc-group=turnserver
<<<<<<<

sudo systemctl start coturn
sudo ufw allow 3478
sudo systemctl status coturn
sudo lsof -i -P -n | grep LISTEN

https://webrtc.github.io/samples/src/content/peerconnection/trickle-ice/

```

