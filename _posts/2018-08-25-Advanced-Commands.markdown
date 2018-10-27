---
layout: post
title:  "Advanced Commands!"
date:   2018-10-4 13:31:20 +0200
categories: Advanced Commands
---

## LIST OF ADVANCED COMMANDS

## Command du and df

### Commans ```du``` 
we use when we want to display number of blocks for files and directorys specified by file and directory arguments.

```du $1```

### Command ```df``` 

we use when we want to get the attributes of all, or the specified file systems on the system.

### Command ```df -m```
we use when we want to display the free memory on hard disk in megabytes

### Command ```df -h```
we use when we want to display the free memory on hard disk in gigabytes

### Command ```df -hT /home
in this example we use the command when we want to display only memory of /home in megabytes and in gigabytes

### Example for creating a symbolic link

```
touch slink
echo some_text > slink
ln -s slink some_text
cat slink
display output:
some_text
``` 

## Linking multiple command plates

Linking multiple commands is achieved by using the symbol pipe, | .
When the shell sees the pipe, it executes the previous command and, after that, creates a link to the standard input of the following commands, in the order in which the commands are in the command line.

### Example


```who | grep $1```

## Command ```sed```
We can use it to edit the file using the script.
In the script we can specify commands of one or more rows, in accordance with the rules that are listed as part of one or more commands.

### Command ```sed -e```
We use the sed -e command when we want to print the numbers of rows in which the specified pattern is found.

#### Example ```sed -e "/ls/=" $1 

## Commands ```sort```
We use when we want to sort the specified file according to the specified order.

#### Example
```sort $1```

### Command ```sort -u```
We use when we want to keep only one row, in the case when the result of sorting appears more same rows.

#### Example 

{% highlight bash %}
sort -u $1
{% endhighlight %}

### Command ```sort -r```
We use if we want to sort the file in reverse order.

#### Example ```sort -r```

### Command ```sort -f```
We use when we want to sort the file in the order of capital letters.

#### Example

```
sort -f
```

### Command ```sort -d```
We use it if we want to sort the file in alphabetical order.

#### Example

```
sort -d
```
