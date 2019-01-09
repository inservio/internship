---
layout: default
title: How to configurate nginx
parent: Nginx
permalink: /docs/nginx/how-to-configurate-nginx/
---

# Introduction 

Configuration Nginx

## Demonstration

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


## Location blocks

Location blocks nalaze se unutar server blocks ili drugih blokova lokacije i koriste se za odlucivanje kako obraditi URL zahtjev.
URL zahtjev je dio koji dolazi nakon naziva domene ili IP adrese /, porta.

````
location optional_modifier location_match {
}
````

* location match definira sta bi Nginx trebao provjeriti uz zahtjev URL.
* Postojanje ili nepostojanje modifikatora u  primjeru ````location optional_modifier location_match```` utjece na nacin na koji se Nginx pokusava uskladiti s blokom lokacije.

### Examples for modifiers

* (none): if no modifiers are present, the location is interpreted as a prefix match

* ````=```` If an equal sign is used, this block will be considered a match if the request URI exactly matches the location given.

* ````~```` If a tilde modifier is present, this location will be interpreted as a case-sensitive regular expression match.

* ````~*```` If a tilde and asterisk modifier is used, the location block will be interpreted as a case-insensitive regular expression match

* ````^~````  If a carat and tilde modifier is present, and if this block is selected as the best non-regular expression match, regular expression matching will not take place.

### Demonstration 

````
location / {
} 
* pretrazuje root location 
````

````
location = /example {
}
* odgovara samo zahtjevu "/example"
````

````
location ^~ /example {
}
* rezultira u case sensitive regular expression koji odgovara slučaju
* to znaci da ce /example, /example/examp.gif, sve biti upareno 
````

````
location ~ example  {
}
* kada location directive sljedi znak ~ nginx obavlja regular expression match.
* te podudarnosti su uvijek case-sensitive.
* tako da bi ````example```` odradio podudarnost ali ````ExAmple```` ne bi
````

````
location ~* /example {
}
* funkcionise kao u prvom primjeru samo je sada insensitive version
````

````
location ~ \. (gif|jpg|)$ {
}
* svi strings se prvo provjeravaju pa onda regular expressions,
* regular expressions se podudaraju redosljedom kojim se pojavljuju u fajlu/datoteci
````

