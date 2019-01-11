---
layout: default
title: Understanding Nginx
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

## Return direvtive 

Da bi koristili direktivu return, ona mora biti zatvorena unutar server ili location blocka koji URL-ovi trebaju biti prepisani.

### Example

````

server {
 listen 80;
 
 server_name www.old-website.com;
 
 return 301 $scheme://www.new-website.com$request_uri;
}
````

U gorenjem primjeru, stara adresa web lokacije odgovara URL-u koji se trazi od klijenta.
Direktiva return bi zatim vratila 301 status code u browser i preusmjerila klijenta na novu adresu web lokacije.

Nginx variabla $scheme koristi se za definiranje protokola (http ili https) dok je $request_uri za potpuni URI


#### 301 status code explain

The HTTP response status code 301 is used for permanent URL redirection, meaning current links or records using the URL that the response is received for should be updated. 
The new URL should be provided in the Location field included with the response. 

### try_files directive

A very common try_files line is 

````
location / {
    try_files $uri $uri/ test/images/index.html;
}
````

* ````location / ```` ima zadatak da odgovara svim lokacijama, osim ako se ne podudara s odredjenom lokacijom, npr lokacija / example.

* Drugi dio ````try_files```` znaci kada primimo URI koji se podudara s ovim blokom, ````try $uri```` na primjer http:/example.com/images/image.jpg nginx ce pkusati provjeriti da li postoji datoteka unutar /images nazvana image.jpg ako pronadje prvo ce posluziti.

* Second condition je $uri/ sto znaci da ako nismo pronasli prvi uvjet $ uri pokusajte URI kao direktorij, npr http://example.com/images/, nginx ce prvo provjeriti da li postoji datoteka koja se zove images, onda ako ne pronajdemo, prelazmo na drugi $uri/ i tu provjeravamo da li postoji direktorij images ako postoji onda ce pokusati posluziti.

* Treci condition /test/index.html;
 
Smatra se fall back option,(moramo koristiti najmanje dvije opcije jednu i povratnu), mozemo koristiti onoliko koliko zelimo, nginx ce traziti datoteku index.html unutar test dir i posluziti ako postoji.
