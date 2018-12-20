---
layout: default
title: WPCLI Database     
parent: Wordpress
---
# WPCLI Database

### MySQL Console

* Login to the Database

````
wp db cli
````

* from mysql console

````
show tables;
````

show all columns from wp_users table.

````
select * from wp_users;
````

show select `id`, `user_login`, `user_email` columns `from wp_users`

````
select id,user_login,user_email from wp_users;
````

* exit MySQL console

````
\q
````

### WP db functions

* WP database Check

````
wp db check
````

* Show columns from table `wp_posts`

````
wp db columns wp_posts
````

* Run a query

````
wp db query "SELECT * FROM wp_options"
````

### Exporting and Importing databas using wp 

* Run the command

````
wp db export example.sql
````

* Importing 

````
wp db import new_example.sql
````
