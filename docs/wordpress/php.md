---
layout: default
title: 02 PHP Setup       
parent: Wordpress
---

# PHP

## Install php packages

```
apt-get -y install php7.0-fpm
```

Install mysql for php
```
apt-get install php7.0-mysql
```

Install gd (GD Graphic library) for php
```
apt-get install php7.0-gd
```

Install zip for php
```
apt-get install php7.0-zip
```

### Restart PHP

````
systemctl restart php7.0-fpm.service
````


Search for other PHP packages

````
apt-cache search php7
````


## Create PHP-FPM pool

````
touch /etc/php/7.0/fpm/pool.d/wartburg.com.conf
````

````
[wartburg_com]

listen = /var/lib/php/wartburg_com.sock

listen.owner = wartburg_com
listen.group = wartburg_com

listen.mode = 0777

user = wartburg_com
group = wartburg_com

rlimit_files = 65535

pm = ondemand
pm.max_children = 40
pm.process_idle_timeout = 10s

pm.status_path = /status

ping.path = /ping
ping.response = pong

chdir = /var/www/wartburg.com

request_terminate_timeout = 300s

php_admin_value[open_basedir] = /var/www/wartburg.com:/usr/share/php5:/usr/share/php::/usr/share/pear:/tmp:/usr/share/phpmyadmin:/etc/phpmyadmin:/var/lib/phpmyadmin
php_admin_value[session.save_path] = 127.0.0.1:11211
php_admin_value[upload_tmp_dir] = /var/www/wartburg.com/tmp
php_admin_value[sendmail_path] = /usr/sbin/sendmail -t -i -fwebmaster@wartburg.com
php_admin_value[opcache.enable] = 0
````

### Restart PHP

````
systemctl restart php7.0-fpm.service
````

### Check if php socket for user was created `wartburg_com`

Each site should have it's own socket file

````
ls /var/lib/php/wartburg_com.sock
````


### Memcached

We will use memcached to store session files

````
apt-get install memcached php7.0-memcached
````

#### Start memcached service

````
systemctl start memcached
````
