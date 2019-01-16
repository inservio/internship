---
layout: default
title: Let's Encrypt - Free Certificate
parent: SSL
---

# How to install

Everything is dona via [certbot](https://certbot.eff.org/).

## install certbot

https://certbot.eff.org/lets-encrypt/debianother-nginx


````
cd /root
wget https://dl.eff.org/certbot-auto
chmod a+x certbot-auto
````

## Getting a certificate

List of [plugins](https://certbot.eff.org/docs/using.html#getting-certificates-and-choosing-plugins).

### webroot plugin

You need to tell cerbot where your root folder, ot webroot, is located at. Find it with `grep` command.

````
grep root /etc/nginx/sites-enabled/domain.com.conf
````

In following example directory `/var/www/html/` is the **webroot**.

````
/root/certbot-auto -m support@domain.org --agree-tos certonly --webroot -w /var/www/html/ -d hostname.domain.com
````

# ISPConfig and Let's Encrypt Free Certificate

Backup expiring/expired certificates.

````
mv /usr/local/ispconfig/interface/ssl/ispserver.key /usr/local/ispconfig/interface/ssl/ispserver.key_BKP
mv /usr/local/ispconfig/interface/ssl/ispserver.crt /usr/local/ispconfig/interface/ssl/ispserver.crt_BKP
````

Link to the new certificates.

````
ln -s /etc/letsencrypt/live/server.domain.com/cert.pem /usr/local/ispconfig/interface/ssl/ispserver.crt
ln -s /etc/letsencrypt/live/server.domain.com/privkey.pem /usr/local/ispconfig/interface/ssl/ispserver.key
````

restart nginx

````
/etc/init.d/nginx restart
````

# PUREFTPD and Let's Encrypt Free Certificate

````
cat /etc/letsencrypt/live/server.domain.com/privkey.pem /etc/letsencrypt/live/server.domain.com/fullchain.pem > /etc/ssl/private/pure-ftpd.pem
````

restart

````
/etc/init.d/pure-ftpd-mysql restart
````
