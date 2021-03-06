---
layout: default
title: WPCLI      
parent: Wordpress
---
# WPCLI

## Install `WPCLI` or Wordpress Command Line Interface

As `root` user

Install curl

````
apt-get install curl
````
Once you’ve verified requirements, download the wp-cli.phar file using wget or curl:

````
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
````

Next, check if it is working:


````
php wp-cli.phar --info
````

To use WP-CLI from the command line by typing wp, make the file executable and move it to somewhere in your PATH. For example:

````
chmod +x wp-cli.phar
````

````
mv wp-cli.phar /usr/local/bin/wp
````

### External Install howto link

[Link](https://make.wordpress.org/cli/handbook/installing/)





# Using `WPCLI`

Login as website user

````
su wartburg_com -l
````

Change directory to website web folder

````
cd /var/www/wartburg.com/web
````

List users

````
wp user list
````

Change password for user with ID `1` which is the admin user

````
wp user update 1 --user_pass=$UP3RstrongP4$$w0rd
````

## Create posts with wpcli

````
wp post create --post_title='A post' --post_content='Just a small post.' --post_status=publish
````

## Set blog name / site name

````
wp option update blogname 'THIS IS MYYYYYY BLOG'
````


# Install and manage wp themes from WP CLI

-Login as user

```
su user -l
```

```
Go to wp site — path /var/www/wordpress
```

- List themes

```
wp theme list
```

Install and activate theme:

```
wp theme install twentyfifteen --activate
```

Activate only - switch to a different theme

````
wp theme activate twentysixteen
````

````
wp theme activate twentyfifteen
````

````
wp theme activate twentyseventeen
````

##### Disable ALL plugins

````
wp db query "UPDATE wp_options SET option_value = '' WHERE option_name = 'active_plugins';"
``````


## Get domain / Set domain

#### Get current domain - `home` and `siteurl`

````
wp option get home
wp option get siteurl
````

#### Set new domain - `home` and `siteurl`

````
wp option update home 'http://old_domain.com'
wp option update siteurl 'http://new_domain.com'
````

or

````
wp search-replace 'http://old_domain.ba' 'http://new_domain.ba'
````


## Security check with WPCLI


````
wp core verify-checksums
````

Force reinstall

````
wp core download --force
````

Update all themes and plugins

````
wp plugin update --all
wp theme update --all
````


## Force reinstall all plugins and themes

````
wp plugin install $(wp plugin list --field=name) --force
wp theme install $(wp theme list --field=name) --force
````

## Disable comments on wp
```
wp post list --format=ids | xargs wp post update --comment_status=closed
```

## Disable plugins on wp
```
$ wp post list --format=ids | xargs wp post update --ping_status=closed
```

## Deleting comments on wp
````
wp comment delete 8 --force
````

## Deleting spam comments on wp
````
wp comment delete $(wp comment list --status=spam --format=ids)
````
