---
layout: default
title: Troubleshooting      
parent: Wordpress
---

## NGINX

* Keep getting `nginx: [emerg] "keepalive_timeout" directive is duplicate` ? That means there is a duplicate `keepalive_timeout` defined already in `/etc/nginx`. To find files that have that keyword use the command below.

````
grep keepalive_timeout /etc/nginx/ -rl
````
