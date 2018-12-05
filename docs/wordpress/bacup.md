---
layout: default
title: Backup      
parent: Wordpress
---

# How to backup a wordpress site

In this example we will backup a website located in `/var/www/site1.com/web` directory.

### Backup MySql database

* check if `mysql-client` package is installed - install it just in case.

````
apt-get install mysql-client
````

### Get the database connection information from the wordpress config file.

````
cd /var/www/site1.com/web
````

* get the mysql server hostname

````
grep DB_HOST /var/www/site1.com/web/wp-config.php
````

* get the mysql username

````
grep DB_USER wp-config.php
````

* get the mysql database name

````
grep DB_NAME wp-config.php
````

* get the mysql password

````
grep DB_PASSWORD wp-config.php
````

#### Backup the database with mysqldump

There is a variable that generates random numbers, test it with following command `echo $RANDOM`. We must have database dump with random number in file names for securty reasons.

````
mysqldump -h DATABASE_HOSTNAME -u DATABASE_USERNAME -p DATABASE_NAME > "DATABASE_NAME_$RANDOM.sql"
````

check if the file was created

````
ls *.sql
````
#### Restore the database with mysql

````
mysql -h DATABASE_HOSTNAME -u DATABASE_USERNAME -p DATABASE_NAME < DATABASE_NAME_$RANDOM.sql
````

## Create archive

````
cd /var/www/site1.com/
tar -cpzf site1.com.tar.gz web/
````

check if the file was created

````
ls *.tar.gz
````

check the usage of the file

````
du -hs *.tar.gz
````
