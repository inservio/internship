---
layout: default
title: Kategorije
permalink: /kategorije/
---

<p>Posts from internship inservio are:</p>

<ul>
{% for post in internship.inservio.ba % }
  {% if post.url %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
 {% endfor %}
</ul>
