---
layout: default
title: User Setup and Wordpress Download       
parent: Wordpress
---

# User Setup

* The name of the user should be associated to the web site name. For example if the name of the web site is wartburg.com then the user with username `wartburg` should be created.

## User setup


### Generate random password

````
RANDOM_PASSWORD=$(head -c 222 /dev/urandom | md5sum| base64)
echo $RANDOM_PASSWORD
````

### Add the user

Use the random generated password as the user's password.

````
adduser wartburg_com
````

* Check for home directory `ls /home/wartburg/`
* Check for user entry in `grep wartburg /etc/passwd`

# Folder setup

## Create directories where to download Wordpress

````
mkdir -p /var/www/wartburg.com/{web,log,tmp}
````

# Wordpress download

* Login as wartbug_com user

````
su wartburg_com -l
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

## Change ownership

If you extracted the wordpress archive as root user then change the ownership as follows.
````
chown -R wartburg_com.wartburg_com /var/www/wartburg.com/web
````
