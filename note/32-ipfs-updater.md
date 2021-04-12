```


cd ~
wget https://dist.ipfs.io/ipfs-update/v1.6.0/ipfs-update_v1.6.0_linux-amd64.tar.gz
tar xvfz ipfs-update_v1.6.0_linux-amd64.tar.gz
cd ipfs-update
sudo ./install.sh
ipfs-update versions
sudo ipfs-update install latest

ipfs init --profile server
ipfs cat /ipfs/QmQPeNsJPyVWPFDVHb77w8G42Fvo15z4bG2X8D2GhfbSXc/readme

sudo apt-get install -y supervisor
sudo vi /etc/supervisor/supervisord.conf
>>>>>
[program:ipfs]
environment=IPFS_PATH=/home/num/.ipfs
command=ipfs daemon
<<<<<
sudo supervisorctl reread && sudo supervisorctl update
sudo supervisorctl status

ipfs swarm peers
ipfs cat QmW2WQi7j6c7UgJTarActp7tDNikE4B2qXtFCfLPdsgaTQ
sudo supervisorctl stop ipfs
vi ~/.ipfs/config
>>>>>>
  "Datastore": {
    "StorageMax": "1GB"
  }

    "Gateway": "/ip4/0.0.0.0/tcp/8080"

    "HTTPHeaders": {
       "Access-Control-Allow-Headers": [
          "X-Requested-With",
          "Access-Control-Expose-Headers",
          "Range"
       ],
       "Access-Control-Expose-Headers": [
          "Location",
          "Ipfs-Hash"
       ],
       "Access-Control-Allow-Methods": [
          "POST",
          "GET"
       ],
       "Access-Control-Allow-Origin": [
          "*"
       ],
       "X-Special-Header": [
          "Access-Control-Expose-Headers: Ipfs-Hash"
       ]
    },
    "RootRedirect": "",
    "Writable": true,
    "PathPrefixes": [],
    "APICommands": [],
<<<<<<
sudo supervisorctl start ipfs

http://node01.popiang.com:8080/ipfs/QmW2WQi7j6c7UgJTarActp7tDNikE4B2qXtFCfLPdsgaTQ/cat.jpg

ipfs swarm peers
ipfs id
ipfs swarm connect <address>

```

