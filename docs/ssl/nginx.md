---
layout: default
title: NginX     
parent: SSL
---

# Howto SSL with NginX

SSL / TLS listens on port `443`.

````
listen IP:443 ssl;
ssl_protocols TLSv1 TLSv1.1 TLSv1.2;
ssl_certificate /etc/letsencrypt/live/domain.ba/fullchain.pem;
ssl_certificate_key /etc/letsencrypt/live/domain.ba/privkey.pem;
 ````

 Test if certificate matches the key

````
ngnix -t
````

### How to redirect http to https

````
if ($scheme != "https") {
  rewrite ^   https://$server_name$request_uri? permanent;
 }
 ````

### How to override amche challenge url

````
        location ~ /\.well-known/acme-challenge/ {
           root /var/www/html/;
           index index.html index.htm;
           try_files $uri =404;
        }
````
