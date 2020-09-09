```

sudo vi /etc/nginx/sites-available/$HOST
>>>>>
    location /ipfs {
        proxy_pass http://localhost:8080;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
<<<<<
sudo nginx -t
sudo systemctl restart nginx

https://node01.popiang.com/ipfs/QmW2WQi7j6c7UgJTarActp7tDNikE4B2qXtFCfLPdsgaTQ/cat.jpg

```

