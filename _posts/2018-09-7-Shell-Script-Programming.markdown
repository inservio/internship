---
layout: post
title:  "Shell Script Programming Category!"
date:   2018-09-7 13:31:20 +0200
categories: SSP category
---

## What's the program?

The program is a set of instructions that cause the computer to perform some useful functions.
In other words, when you specify a computer to perform some tasks in a certain order, so that the overall result is better than the result of individual tables, you have programm$

### Output data from the shell program

The echo command recognizes several special escape characters, which help in formatting the output.
These are the following characters:

\b - Backspace

\c - Ispisuje red bez karaktera za novi red

\f - Form Feed: na stampacu pomjera se za stranicu unaprijed, na ekranu terminala prelazi se na novi ekran.

\n - Newline

\r - Carriage return

\t - Tab

\v - Vertikalni tab

\ / - Backslash

\ 0nnn - Jednocifreni, dvocifreni, ili trocifreni oktalni cijeli broj koji predstavlja jedan od ASCII karaktera


#### Example
If we want to prompt the user to enter the data, in which case you want the user's response to appear in the same line as the prompt, use the \ c character.

``` "Guns N' Roses:\c" ```


## Inserting comments in shell programs
When writing programs, it often happens that you do not have a clear program code that was logical six months ago.
In order to make our programs easier, we mark comments. We enter the comments in the shell programs by setting a special character (#).
When a shell interpreter sees a character (#), it considers the whole text as a commentary to the end of the line.

## If-then-else command

During programming we usually want to perform one set of commands if the condition is met and the second set of commands if the condition is not met.
In the shell, this can be achieved if you use the if-then-else construction.

#### Example for if-then-else construction

```if [1 -lt 100]
then
echo "Correct"
else
echo "Not Correct"
fi```

Display the output
"Correct"
Because 1 is less than 100.

## Making decisions in shell programs
One of the advantages that gives computer programming languages great power is their ability to make decisions.
Of course, computers are not able to think, so the decisions that programs bring on the computer represent only the answer to the conditions that you predicted in your program.
Decisions made by programs on the computer are in the form of conditional execution:
-if there is a requirement, then a specific set of commands is executed.
In most computer languages, this command is called if-then construction.

#### Example for if-then construction
Command if-then example
Combine the command ls -a -l and display the length of the list.
```if ls
then
ls -a
ls -l
fi```

Perform arithmetic operations over shell variables

Variables are typed in most programming languages, which means they are limited to certain types of data, such as numbers or characters. Shell variables are always remembered as $

expr integer operator integer

The following operators are the important arithmetic operators:
(+)Sets two whole numbers

(-)It subtracts the second full integer from the first full integer.

(*) There are two integer numbers (When we want to multiply two integers in the terminal we have to use the correct format for multiplication, which is "expr 4 * 5")

(/) The first integer is shared by another integer.

(%) Gives the module (rest) of the sharing.

#### Examples

Example arithmetic addition operation + "
Example 2 + 1

```expr 2 + 1```

Example arithmetice subtraction - "
Example 5 - 4

```expr 5 - 4```

Example arithmetic multiplication operation * but the the correct form of multiplication in the terminal is \* "
Example 7 \* 8"

```expr 7 \* 8```

Example arithmetic division operation / "
Example 6 / 2

```expr 6 / 2```

Arithmetic terms can also be combined, as in the following example:
Example 6 + 7 / 3
```expr 6 + 7 / 3```

Command expr does not recognize brackets, which is why you need to manually override the priority, if there is a need for it.
We can use backward characters to change priority rights, in the following way:
Example
```int = expr 6 + 7```
```expr int / 3```

```int= `expr 6 + 7` ```
```expr $int / 3```

Or we can use a more direct route:
Example expr 6 + 7' / 3

```expr `expr 6 + 7` / 3```
