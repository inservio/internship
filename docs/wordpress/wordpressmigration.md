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

Moj prvi korak je bio logovanje na sourceserver -p 2222
Onda sam urdio navigaciju na /var/www, pronasao sam direktorij example.

Pogledao sam sve fajlove i ostale direktorije uradio sam kompletan pregled dokumentacije.

Zadatak koji sam dobio je migracija fajlova u novi direktorij pod nazivom newexample.com

Takodjer trebam podici i na novi hosing https://destinationserver.com:10000/

Ja sam shvatio da trebam koristiti mysql i wp alatku. Moja vizija i zamisao rijesavanja ovog zadatka je sljedeca:

Kreiram novi direktorij komandom mkdir -p /var/www/newdirectory.com{web,tmp,log}

Izvrsim odredjene izmjene u nginx novi nginx conf

## Questions
* 1)Iz kojeg foldera radimo migraciju ?
* Odgovor: Uradimo navigaciju na source server /var/www/directory.com/web  
* 2)Na koji server radimo migraciju ? 
* Odgovor: Migraciju radimo na zeljeni destination server
* 3)Sa kojeg servera vrsimo migraciju ?
* Odgvor: Migraciju vrsimo sa zeljenog source servera
* 4) U koji folder radimo migraciju ?
* Odgovor: Uradimo navigaciju na destination server /var/www/newdirectory.com/web
* 5) Lista protokol 
* 6) Odgovor: FTP, SSH u momo slucaju je SSH protokol


### Korak 1
Stavka napraviti arhivu: 


````
* Nalazim se na  source serveru
$ cd /var/www/directory.com/
$ tar -cpzf directory.com.tar.gz
````

### Korak 2 
Stavka uraditi backup baze komandom
````
mysqldump -h DATABASE_HOSTNAME -u DATABASE_USERNAME -p DATABASE_NAME > "DATABASE_NAME_$RANDOM.sql"
````
* Na sourceserveru
* login kao wp user su user
* Uraditi navigaciju u /var/www/directory.com/web/

Provjeravam host sljedecom komandom ```` grep DB_HOST  wp-config.php````
Provjeravam database_username ````grep DB_USER wp-config.php````
Provjeravam database_name ````grep DB_NAME wp-config.php````

### Korak 3
Stavka option rsync
Uraditi rsync directories

Instalirati rsync komandom ````apt-get install rsync````

````
rsync -avz -e 'ssh -p 22' /var/www/sourceserver/web/examplefile.sql databasename@sourceservere:/var/www/newdirectory.com/web
````
### Korak 4
Sljedeci korak uraditi restore tar.gz arhive komandom

* Nalazim se na destination serveru

````tar -xzvf archive.tar.gz````

### Korak 5
Onda uraditi import database
mysql -h DATABASE_HOSTNAME -u DATABASE_USERNAME -p DATABASE_NAME < DATABASE_NAME.sql

### Korak 6
Dodijeliti odredjene permissions 
* Nalazim se na  destination serveru
* Postavljam permissions za modifikovanje fajlova

````chown -R newuser.newuser /var/www/newdirectory.com/web````

* Nalazim se na destination serveru

### Korak 7
I na kraju izvrsiti izmjene u /var/www/newdirectory.com/web/wp-config.php fajlu

* komandom nano wp-config.php

Promjeniti username
Pormjeniti password
Promjeniti databse

