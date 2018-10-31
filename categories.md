---
layout: default
title: Categories
permalink: /categories/
---

<p>Posts from internship inservio are:</p>

<ul>
{% for post in site.categories.DNS category %}
  {% if post.url %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}	 
{% endfor %}
</ul>
