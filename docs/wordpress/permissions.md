---
layout: default
title: File permissions      
parent: Wordpress
---

# File permissions

Observe what happens when you try to access files after this changes

## Others permissions

Remove read permissions for `others`

````
chmod o-r /var/www/domain.com/web -R
ls -al /var/www/domain.com/web
````

## User permissions

Remove read permissions for `user`

````
chmod u-r /var/www/domain.com/web -R
ls -al /var/www/domain.com/web
````


## Group permissions

Remove read permissions for `group`

````
chmod g-r /var/www/domain.com/web -R
ls -al /var/www/domain.com/web
````


# Restore permissions

````
chmod o+r /var/www/domain.com/web -R
chmod u+r /var/www/domain.com/web -R
chmod g+r /var/www/domain.com/web -R
ls -al /var/www/domain.com/web
````

or

````
chmod 755 /var/www/domain.com/web -R
ls -al /var/www/domain.com/web
````
