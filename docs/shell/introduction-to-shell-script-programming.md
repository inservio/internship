---
layout: default
title: Shell Script Programming
parent: Shell
permalink: /docs/shell/introduction-to-shell-script-programming/
---

## What's the program?

The program is a set of instructions that cause the computer to perform some useful functions.
In other words, when you specify a computer to perform some tasks in a certain order, so that the overall result is better than the result of individual tables, you have programm$

### Output data from the shell program

The echo command recognizes several special escape characters, which help in formatting the output.
These are the following characters:

`\b` - Backspace

`\c` - Ispisuje red bez karaktera za novi red

`\f` - Form Feed: na stampacu pomjera se za stranicu unaprijed, na ekranu terminala prelazi se na novi ekran.

`\n` - Newline

`\r` - Carriage return

`\t` - Tab

`\v` - Vertikalni tab

`\` / - Backslash

`\` 0nnn - Jednocifreni, dvocifreni, ili trocifreni oktalni cijeli broj koji predstavlja jedan od ASCII karaktera


#### Example

If we want to prompt the user to enter the data, in which case you want the user's response to appear in the same line as the prompt, use the \ c character.

``` "Guns N' Roses:\c" ```
