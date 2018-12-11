---
layout: default
title: PHP Opcache Setup       
parent: Wordpress
---

# PHP Opcache

Opcache will speed your PHP web site. This article will explain how to enable and configure the site.

## Install php opcache packages

For PHP version 5.6

```
apt-get install php5.6-opcache
```

To find opcache package matching your PHP version do a search using following command

````
apt-cache search opcache
````

* Search if enabled/disabled in fpm pool

For PHP 5.6 version

````
grep opcache /etc/php/5.6/fpm/pool.d/*
````

If you get results you need to enable opcache in every fpm pool like This

````
php_admin_value[opcache.enable] = 1
````

### Enable Opcache in php.ini

In this example we will

* enable opcache,
* set amount of RAM memory opcache will use,
* set the number of files that can be cached,
* set the revalidate frequency - this tells the cache how often to check the timestamp on the files, how ofthen the file has been changed. This is measured in seconds.

````
[opcache]
opcache.enable=1
opcache.memory_consumption=128
opcache.max_accelerated_files=4000
opcache_revalidate_freq=240
````
### Enable opcache module

````
php5enmod opcache
````

For other PHP versions

````
phpenmod opcache
````

### Check if enabled

For php 5.6

````
cat /etc/php/5.6/fpm/conf.d/*-opcache.ini
````

### Check phpinfo() for your site

create a file named `info.php` and put it inyour web root folder.

````
<?php
phpinfo();
?>
````

Search for opcache. Is it enabled?


### Restart php

````
/etc/init.d/php5.6-fpm restart
 ````
