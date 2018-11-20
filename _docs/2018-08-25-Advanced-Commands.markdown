---
layout: single
title:  "Advanced Commands!"
date:   2018-10-4 13:31:20 +0200
categories: ac
---

## LIST OF ADVANCED COMMANDS

## Command du and df

### Command ```du```
we use when we want to display number of blocks for files and directorys specified by file and directory arguments.

### Command ```df```

we use when we want to get the attributes of all, or the specified file systems on the system.

Another option for df command ```df -m```
we use when we want to display the free memory on hard disk in megabytes

Another option for df command ```df -h```
we use when we want to display the free memory on hard disk in gigabytes

Another option for df command ```df -hT /home```
in this example we use the command when we want to display only memory of /home in megabytes and in gigabytes

### Example for creating a symbolic link

{% highlight bash %}
touch slink
echo some_text > slink
ln -s slink some_text
cat slink
display output:
some_text
{% endhighlight bash %}

## Linking multiple command plates

Linking multiple commands is achieved by using the symbol pipe, | .
When the shell sees the pipe, it executes the previous command and, after that, creates a link to the standard input of the following commands, in the order in which the commands are in the command line.

### Example

{% highlight bash %}
who | grep $1
{% endhighlight bash %}

## Command ```sed```
We can use it to edit the file using the script.
In the script we can specify commands of one or more rows, in accordance with the rules that are listed as part of one or more commands.

Another option for sed command ```sed -e```
We use the sed -e command when we want to print the numbers of rows in which the specified pattern is found.

#### Example
{% highlight bash %}
sed -e "/ls/=" $1
{% endhighlight bash %}

## Commands ```sort```
We use when we want to sort the specified file according to the specified order.

#### Example
{% highlight bash %}
sort $1
{% endhighlight bash %}

Another option for sort command ```sort -u```
We use when we want to keep only one row, in the case when the result of sorting appears more same rows.

#### Example

{% highlight bash %}
sort -u $1
{% endhighlight %}

Another option for sort command ```sort -r```
We use if we want to sort the file in reverse order.

#### Example
{% highlight bash %}
sort -r
{% endhighlight bash %}

Another option for sort command ```sort -f```
We use when we want to sort the file in the order of capital letters.

#### Example
{% highlight bash %}
sort -f
{% endhighlight bash %}

Another option for sort command ```sort -d```
We use it if we want to sort the file in alphabetical order.

#### Example
{% highlight bash %}
sort -d
{% endhighlight bash %}

## Command ```uniq```
We use when we want to eliminate duplicate adjacent rows from a file, or from a standard input, in order to generate a standard output, or another file.

#### Example
{% highlight bash %}
uniq $1
{% endhighlight bash %}

Another option for uniq command ```uniq -u```
We use when we want to display rows that appear only once in the file.

#### Example
{% highlight bash %}
uniq -u $1
{% endhighlight bash %}

Another option for uniq command ```uniq -f```
We use when we want to skip rows.

{% highlight bash %}
uniq -f $1
{% endhighlight bash %}

Another option for uniq command ```uniq -d```
We use when we want to display only duplicate rows.

{% highlight bash %}
uniq -d $1
{% endhighlight bash %}

## Entering the commands that are processed in the background

Shell provides the ability to handle commands in the background.
This is achieved by setting the ampersand symbol, &, to the end of the command.

{% highlight bash %}
find / -name "$1" -print > find.results 2>/dev/null &
{% endhighlight bash %}

## Enter multiple commands in one row
Usually, shell interprets the first word from the command input as the command name, and the rest of the input as an argument for that command.
A special shell character, a dot-comma (;), tells the shelf that the text of the previous command has ended and that what comes next behind this character is a new command.

### Example
{% highlight bash %}
find $1; ls $2; pwd $3
{% endhighlight bash %}

## Command whereis

We use it to search binary files, as well as other commands, source and manual pages.

#### Example
{% highlight bash %}
whereis $1
{% endhighlight bash %}

Another option for whereis command ``` whereis -m```
We use it to search for manual page of some program.

#### Example
{% highlight bash %}
whereis -m $1
{% endhighlight bash %}

Another option for whereis command ```whereis -b```
We use it to search for binary files.

{% highlight bash %}
whereis -b $1
{% endhighlight bash %}
