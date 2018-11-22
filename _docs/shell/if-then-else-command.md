---
layout: single
title: If then else commands
parent: Shell
permalink: /docs/shell/if-then-else-command/
---

{% include base_path %}

During programming we usually want to perform one set of commands if the condition is met and the second set of commands if the condition is not met.
In the shell, this can be achieved if you use the if-then-else construction.

#### Example for if-then-else construction

{% highlight ruby %}
if [1 -lt 100]
  then
    echo "Correct"
  else
    echo "Not Correct"
fi
{% endhighlight ruby %}

#### Display the output

{% highlight ruby %}
Correct
Because 1 is less than 100.
{% endhighlight ruby %}


