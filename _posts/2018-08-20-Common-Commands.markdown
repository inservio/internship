---
layout: post
title:  "Common Commands!"
date:   2018-10-4 13:31:20 +0200
categories: Common Commands
---

## The most common command in Linux/Unix is ```ls```.
We use ```ls``` command to list files from the current directory.
To list all hidden files we use ```ls -a or ls --all```.We can also combine these commands ```ls -a -l```
The command ```ls -l``` changes the format in whic the directory list is displayed, and for each file it displays specific information about it.
We can also combine these commands ```ls -a -l```

With the command ```wc -l``` we get the number of rows in the input.

## Command ```cat``` 
takes the characters from the standard input and, as an echo, sends them to the standard output.

## Commands (cp, mv, rm)

-cp - copy the file
-mv - move the file
-rm - remove the file 

#### Example

```mv ~/Downloads/sound.mp3 ~/Documents/Music```

## Command echo 
we use if we want to display the current value of one variable.

Example
```echo $1``` 

## Command env
will show the user environment.

Example
```env```

Command printenv | grep HOME
we use it when we want to filter env to display only env HOME.

Exaxmple
```print | grep HOME```

Escaping characters quotes ("") or (\) backslash
For example we can use escaping characters for creating a fie with a space in the name.

If we want to escape one character we use ```\```.
For escaping more words, we use single```'``` or double quotes```""```.

## Command mkdir mkdir -p mkdir --parents rmdir
We use it when we want to create a directory.
And then with the command ```rmdir``` we use when we want to delete a directory.
