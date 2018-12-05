---
layout: default
title: If then else commands
parent: Shell
permalink: /docs/shell/if-then-else-command/
---

# Introduction

During programming we usually want to perform one set of commands if the condition is met and the second set of commands if the condition is not met.
In the shell, this can be achieved if you use the if-then-else construction.

## Demonstration

### Example for if-then-else construction

{% highlight bash %}
if [1 -lt 100]
  then
    echo "Correct"
  else
    echo "Not Correct"
fi
{% endhighlight bash %}

#### Display the output

{% highlight bash %}
Correct
Because 1 is less than 100.
{% endhighlight bash %}
