---
layout: default
title: Categories
permalink: /categories/
---

<p>Posts from <strong>test</strong> category are:</p>

<ul>
{% for post in site.categories.test %}
  {% if post.url %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}	 
{% endfor %}
</ul>

<p>Posts from <strong>proc</strong> category are:</p>

<ul>
{% for post in site.categories.proc %}
  {% if post.url %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}	 
{% endfor %}
</ul>

<p>Posts from <strong>regex</strong> category are:</p>

<ul>
{% for post in site.categories.regex %}
  {% if post.url %}
	<li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}	 
{% endfor %}
</ul>
