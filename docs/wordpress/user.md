---
layout: default
title: 0 Wordpress Setup       
parent: Wordpress
---

# User Setup

* The name of the user should be associated to the web site name. For example if the name of the web site is wartburd.com then the user with username `wartburg` should be created.

## User setup


### Generate random password

````
RANDOM_PASSWORD=$(head -c 222 /dev/urandom | md5sum| base64)
echo $RANDOM_PASSWORD
````

### Add the user

````
adduser wartburg
````

* Check for home directory `ls /home/wartburg/`
* Check for user entry in `grep wartburg /etc/passwd`

# Folder setup

## Create directories where to download Wordpress

````
mkdir -p /var/www/wartburg.com/{web,log,tmp}
````

# Wordpress download

* Login as wartbug user

````
su wartburg -l
````

* Change current directory where we will download Wordpress

````
cd /var/www/wartburg.com/web
````

* Download wordpress

````
wget https://wordpress.org/latest.zip
````

* Unzip the latest.zip ZIP archive we just downloaded.

````
unzip latest.zip
````

* The files from the archive have been extracted to the wordpress directory but we need them in the current directory so we move them to `.`

````
mv wordpress/* .
````

* Delete the wordpress directory since we do not need it anymore

````
rm -rf wordpress/
````

* Check if the files are in the web Folder

````
ls /var/www/wartburg.com/web
````
