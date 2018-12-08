---
layout: default
title: Remote copy files      
parent: Wordpress
---

# How to copy a backup archive to remote host

In this example we will copy a `file.tar.gz` owned by `blatusa_com` user located in `/home/blatusa_com` to user `blatusa_clone_com` on `localhost` server.

## Check if current user has generated a key pair.

````
su blatusa_com -l
whoami
cat ~/.ssh/id_rsa.*
````

if not generate it

````
ssh-keygen -t rsa
````

if the key was generated copy it to remote users's home directory

````
ssh-copy-id -i ~/.ssh/id_rsa blatusa_clone_com@localhost -p 22
````

enter password for `blatusa_clone_com` user.

Once the key was added try login via ssh to check if login will work but this time without password.

````
ssh blatusa_clone_com@localhost -p 22
````

If the login work proceed to file copy operation.

## Copy a file via `SCP`

````
scp -P 22 /home/blatusa_com/file.tar.gz blatusa_clone_com@localhost:/home/blatusa_clone_com/
````


File `/home/blatusa_com/file.tar.gz` will be copied to server `localhost` to directory `/home/blatusa_clone_com/` over port `22`.
