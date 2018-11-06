---
layout: post
title:  "Introduction To The Nginx!"
date:   2018-10-4 13:31:20 +0200
categories: nginx
---

## NGINX

NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. 

## Installation and configuration nginx

To install nginx we need to log in to our server

```ssh root@yourserver.com```

##### Next step 
We use the comman ```apt-get update``` just to make sure we have all the latest version of the available package..

Then we use the command ```apt-get install nginx''' or if you are using mac then the replacement form the apt i command ```brew nginx```.

To confirm that nginx is runing we can search for nginx process.
We use the command ```ps aux | grep nginx```.

We can test this in browser by searching for your server ip adress.
Use the command ```ifconfig```

###### Example:
http://yourserveripadress
It should display the nginx welcome page. 

Path to nginx is: /etc/nginx !

### Building Nginx from source and adding modules 

Connect to your server root@yourserver.com !

Then go to ngix.org, click the download link and there you will have the sourec code links.
We can use mainline version.
Copy the link and go to the terminal and downloade the source code.

Use the command ```curl http://nginx.org/download/nginx-1.13.10.tar.gz```

Check the content of this directory command ```ls -l```

## Configuration Nginx

Two main configuration terms are context and directives.

Directives are specific configuration options that get set in the configuration file.
It consists of:
```server_name(name) and a mydomain.com(value)```

Context are sections within the configuration where directives can be set for that given context.
Example main context

```
http{ (for anything http related)
  index index.html index.htm index.php;
	
server{ (here we define the virtual host)
  listen 80;
  server_name mydomain.com;
  access_log /var/www/mydomain/web/access.log;
  error_log /var/www/mydomain/web/error.log;	
  root /var/
	
location{ (for matching url locations on incoming request to the parents server context)
  my_location;	
    }
  

  }
}
```
##### Tip
When we modifie any .conf file we have to use command ```service nginx reload```
And to chech if syntax is ok we use the command ```nginx -t```

