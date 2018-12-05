---
layout: default
title: Restore      
parent: Wordpress
---

# How to restore


## Restore a TAR.GZ archive

````
tar -xzvf archive.tar.gz
````

* x - extract
* z - zip
* v - verbose, show output
* f - file


## Restore the database with mysql

````
mysql -h DATABASE_HOSTNAME -u DATABASE_USERNAME -p DATABASE_NAME < DATABASE_NAME_$RANDOM.sql
````
