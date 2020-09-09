```

cd ~
wget https://dist.ipfs.io/go-ipfs/v0.6.0/go-ipfs_v0.6.0_linux-amd64.tar.gz
tar xvfz go-ipfs_v0.6.0_linux-amd64.tar.gz go-ipfs/
cd go-ipfs
sudo ./install.sh
ipfs init --profile server
ipfs cat /ipfs/QmQPeNsJPyVWPFDVHb77w8G42Fvo15z4bG2X8D2GhfbSXc/readme
ipfs daemon

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

