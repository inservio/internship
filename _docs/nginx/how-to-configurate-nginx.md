---
layout: default
title: How to configurate nginx
parent: Nginx
nav_order: 3
---



### Configuration Nginx

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



