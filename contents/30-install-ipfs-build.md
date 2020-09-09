wget -c https://storage.googleapis.com/golang/go1.15.1.linux-amd64.tar.gz
sudo tar -xvf go1.15.1.linux-amd64.tar.gz
sudo mv go /usr/local
vi ~/.bash_profile
>>>>>>
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export PATH=$GOPATH/bin:$GOROOT/bin:$PATH
<<<<<<
source ~/.bash_profile

sudo apt-get install -y build-essential
git clone https://github.com/ipfs/go-ipfs.git
cd go-ipfs
make install

sudo ipfs init --profile server
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
