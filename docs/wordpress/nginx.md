---
layout: default
title: 1 NginX Setup      
parent: Wordpress
---

# NGINX


### Install nginx package

```
apt-get update
apt-get install nginx zip unzip
```

# Restart *nginx*

```
systemctl start nginx
```

### Create .conf file in /etc/nginx/sites-available/

## Use absolute paths

````
touch /etc/nginx/sites-available/wartburg.com.conf
````

## Edit wartburg.com.conf file

````
nano /etc/nginx/sites-available/wartburg.com.conf
````

##### Paste contents

````
server {
        listen 80;

        server_name wartburg.com *.wartburg.com;

        root   /var/www/wartburg.com/web;

        access_log off;

        index index.html index.htm index.php;

        location ^~ /login {
          return 301 http://wartburg.com/wp-login.php;
        }

        location ^~ /admin {
          return 301 http://wartburg.com/wp-login.php;
        }

        location / {
	        try_files $uri $uri/ /index.php?$args;
        }

        location ~ \.php$ {
            try_files $uri =404;
            include /etc/nginx/fastcgi_params;
            fastcgi_pass unix:/var/lib/php/wartburg_com.sock;
            fastcgi_index index.php;
            fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
            fastcgi_intercept_errors on;
        }

        # Add trailing slash to */wp-admin requests.
        rewrite /wp-admin$ $scheme://$host$uri/ permanent;

}

````

## Enable nginx vhost file

###### Link file from /etc/nginx/sites-available/ to /etc/nginx/sites-enable/

````
$ ln -s /etc/nginx/sites-available/wartburg.com.conf /etc/nginx/sites-enabled/wartburg.com.conf
````

###### Check if symbolic link was properly created

````
ls /etc/nginx/sites-enabled/wartburg.com.conf
````

````
ls -al /etc/nginx/sites-enabled/wartburg.com.conf
````

````
cat /etc/nginx/sites-enabled/wartburg.com.conf
````

### Reload nginx service

````
$ systemctl reload nginx.service
````

## Cloudflare

This setup will show the real visitor IP instead of CloudFlare Proxy IP.

````
nano /etc/nginx/conf.d/cloudflare.conf
````

````
set_real_ip_from 103.21.244.0/22;
set_real_ip_from 103.22.200.0/22;
set_real_ip_from 103.31.4.0/22;
set_real_ip_from 104.16.0.0/12;
set_real_ip_from 108.162.192.0/18;
set_real_ip_from 131.0.72.0/22;
set_real_ip_from 141.101.64.0/18;
set_real_ip_from 162.158.0.0/15;
set_real_ip_from 172.64.0.0/13;
set_real_ip_from 173.245.48.0/20;
set_real_ip_from 188.114.96.0/20;
set_real_ip_from 190.93.240.0/20;
set_real_ip_from 197.234.240.0/22;
set_real_ip_from 198.41.128.0/17;
set_real_ip_from 2400:cb00::/32;
set_real_ip_from 2606:4700::/32;
set_real_ip_from 2803:f800::/32;
set_real_ip_from 2405:b500::/32;
set_real_ip_from 2405:8100::/32;
set_real_ip_from 2c0f:f248::/32;
set_real_ip_from 2a06:98c0::/29;

# use any of the following two
real_ip_header CF-Connecting-IP;
#real_ip_header X-Forwarded-For;
````


[Link](https://support.cloudflare.com/hc/en-us/articles/200170706-How-do-I-restore-original-visitor-IP-with-Nginx-)


## Proxy Params Config

````
nano /etc/nginx/proxy_params
````

````
# time out settings
proxy_connect_timeout 300s;
proxy_send_timeout 600;
proxy_read_timeout 600;
proxy_buffer_size 64k;
proxy_buffers 16 32k;
proxy_busy_buffers_size 64k;
proxy_temp_file_write_size 64k;
proxy_pass_header Set-Cookie;
proxy_redirect off;
proxy_hide_header Vary;
proxy_set_header Accept-Encoding '';
proxy_ignore_headers Cache-Control Expires;
proxy_set_header Referer $http_referer;
proxy_set_header Host $host;
proxy_set_header Cookie $http_cookie;
proxy_set_header X-Real-IP $remote_addr;
proxy_set_header X-Forwarded-Host $host;
proxy_set_header X-Forwarded-Server $host;
proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
````

## Size Limits

````
nano /etc/nginx/conf.d/size_limits.conf
````

````
##
## Size Limits
##
client_body_buffer_size 1k;
client_header_buffer_size 1k;
client_max_body_size 1024m;
large_client_header_buffers 3 3k;
connection_pool_size 256;
request_pool_size 4k;
server_names_hash_bucket_size 128;
````


## Timeouts

````
nano /etc/nginx/conf.d/timeouts.conf
````

````
##
## Timeouts
##
client_body_timeout 60;
client_header_timeout 60;
keepalive_timeout 75 20;
send_timeout 60;
````


## enable gzip compression


````
nano /etc/nginx/conf.d/gzip.conf
````

```
##
# Gzip Settings
##
gzip on;
gzip_disable "msie6";
gzip_vary on;
gzip_proxied any;
gzip_comp_level 6;
gzip_buffers 16 8k;
gzip_http_version 1.1;
gzip_min_length 256;
gzip_types text/plain text/css application/json application/x-javascript application/javascript text/xml application/xml application/xml+rss text/javascript application/vnd.ms-fontobject application/x-font-ttf font/opentype image/svg+xml image/x-icon;
```

## Nginx test configuration

````
nginx -t
````

## Read Nginx Logs

### Access Logs

````
tail -f /var/log/nginx/access.log
````
### Error logs

````
tail -f /var/log/nginx/error.log
````
