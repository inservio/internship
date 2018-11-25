---
layout: default
title: Logic
parent: Ruby
permalink: /docs/ruby/logic/
---

## Logic operators in ruby

````
&& (and)
|| (or)
! (not)
!= (not equal)
== (equal)
>= (greater-than-equal)
<= (less-than-equal)
true
false
````

## The Truth Tables

{% highlight ruby %}
# NOT 	true?
!false 	true
!true 	false
{% endhighlight ruby %}


{% highlight ruby %}
# OR (||) 	true?
true || false 	true
true || true 	true
false || true 	true
false || false 	false
{% endhighlight ruby %}


{% highlight ruby %}
AND (&&) 	true?
true && false 	false
true && true 	true
false && true 	false
false && false 	false
{% endhighlight ruby %}


{% highlight ruby %}
NOT OR 	true?
not (true || false) 	false
not (true || true) 	false
not (false || true) 	false
not (false || false) 	true
{% endhighlight ruby %}


{% highlight ruby %}
NOT AND 	true?
!(true && false) 	true
!(true && true) 	false
!(false && true) 	true
!(false && false) 	true
{% endhighlight ruby %}


{% highlight ruby %}
!= 	true?
1 != 0 	true
1 != 1 	false
0 != 1 	true
0 != 0 	false
{% endhighlight ruby %}


{% highlight ruby %}
== 	true?
1 == 0 	false
1 == 1 	true
0 == 1 	false
0 == 0 	true
{% endhighlight ruby %}
