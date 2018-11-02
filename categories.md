---
layout: default
title: Categories
permalink: /categories/
---

<p>Posts from internship inservio are:</p>

<ul>
{% for post in site.categories.test %}
  {% if post.url %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}	 
{% endfor %}
</ul>

<ul>
{% for post in site.categories.proc %}
  {% if post.url %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}	 
{% endfor %}
</ul>
