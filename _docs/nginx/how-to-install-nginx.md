---
layout: single
title: How to install nginx
parent: Nginx
permalink: /docs/nginx/how-to-install-nginx/
---

{% include base_path %}


## NGINX

NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more.

## Installation and configuration nginx

To install nginx we need to log in to our server

```ssh root@yourserver.com```

##### Next step
We use the comman ```apt-get update``` just to make sure we have all the latest version of the available package..

Then we use the command ```apt-get install nginx```.
If you are using mac then the replacement for the apt is command ```brew nginx```.

To confirm that nginx is runing we can search for nginx process.
We use the command ```ps aux | grep nginx```.

We can test this in browser by searching for your server ip adress.
Use the command ```ifconfig```

###### Example:
http://yourserveripadress
It should display the nginx welcome page.

Path to nginx is: /etc/nginx !

