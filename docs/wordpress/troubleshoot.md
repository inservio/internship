---
layout: default
title: Troubleshooting      
parent: Wordpress
---

## NGINX

### `directive is duplicate`

* Keep getting `nginx: [emerg] "keepalive_timeout" directive is duplicate` ? That means there is a duplicate `keepalive_timeout` defined already in `/etc/nginx`. To find files that have that keyword use the command below.

````
grep keepalive_timeout /etc/nginx/ -rl
````

### Bad gateway

This means nginx is tring to connect to PHP service and either the service is down or the path to the PHP socket is wrong.

Solution is to check the socket and service status.

* Check socket in NginX and PHP

````
grep '\.sock' /etc/php/ -r
````

compare with

````
grep '\.sock' /etc/nginx/sites-available/ -r
````

* Check PHP service status

 first check php service name

 ````
 systemctl list-units | grep php
 ````

 check php service status

 ````
 systemctl status php7.0-fpm.service
 ````
