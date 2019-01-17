---
layout: default
title: How to migrate a WordPress site 
parent: Wordpress
---

# Introduction

Sometimes client will tell you that they're unhappy at their current host and then we will need to help migrate their WordPress site to an new host.

I will show you how to do wordpress migration.

What we will need is:

* Back up clients website files.

* Export the database 

* Create archive of database

* Create a new directory and a new database

* Move the archive.tar.gz file to your new destination

* Import the database to new destination

* Edit wp-config.php

* Edit nginx.conf file


## Demostration and example

Moj prvi korak je bio logovanje na example.inservioserver.com -p 2222
Onda sam urdio navigaciju na /var/www, pronasao sam direktorij example.

Pogledao sam sve fajlove i ostale direktorije uradio sam kompletan pregled dokumentacije.

Zadatak koji sam dobio je migracija fajlova u novi direktorij pod nazivom newexample.com

Takodjer trebam podici i na novi hosing https://newexample.com:10000/

Ja sam shvatio da trebam koristiti mysql i wp alatku. Moja vizija i zamisao rijesavanja ovog zadatka je sljedeca:

Kreiram novi direktorij komandom mkdir -p /var/www/newexample.com{web,tmp,log}

Izvrsim odredjene izmjene u nginx novi nginx conf


Stavka napraviti arhivu: 


````
$ cd /var/www/example.com/
$ tar -cpzf example.com.tar.gz
````



Stavka uraditi backup baze komandom
````
mysqldump -h DATABASE_HOSTNAME -u DATABASE_USERNAME -p DATABASE_NAME > "DATABASE_NAME_$RANDOM.sql"
````

Provjeravam host sljedecom komandom ```` grep DB_HOST  wp-config.php````
Provjeravam database_username ````grep DB_USER wp-config.php````
Provjeravam database_name ````grep DB_NAME wp-config.php````

Stavka option rsync
Uraditi rsync directories

Instalirati rsync komandom ````apt-get install rsync````

````
rsync -avz -e 'ssh -p 22' /var/www/example.com/web/example.sql databasename@examplenameserver.inservioserver.com:/var/www/newexample.com/web
````
Sljedeci korak uraditi restore tar.gz arhive komandom

````tar -xzvf archive.tar.gz````

Onda uraditi import database
mysql -h DATABASE_HOSTNAME -u DATABASE_USERNAME -p DATABASE_NAME < DATABASE_NAME.sql

Dodijeliti odredjene permissions 

````chown -R newuser.newuser /var/www/example.com/web````

I na kraju izvrsiti izmjene u wp-config.php fajlu

Promjeniti username
Pormjeniti password
Promjeniti databse

(Working on this more)
