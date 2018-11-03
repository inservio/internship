---
layout: default
title: Categories
permalink: /categories/
---

<p>Posts from <strong>common commands</strong> category are:</p>

<ul>
{% for post in site.categories.cc %}
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

<p>Posts from <strong>advanced commands</strong> category are:</p>

<ul>
{% for post in site.categories.ac %}
  {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

<p>Posts from <strong>shell scripting</strong> category are:</p>

<ul>
{% for post in site.categories.ss %}
  {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

<p>Posts from <strong>shell variables</strong> category are:</p>

<ul>
{% for post in site.categories.sv %}
  {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

<p>Posts from <strong>network commands</strong> category are:</p>

<ul>
{% for post in site.categories.nc %}
  {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

<p>Posts from <strong>dns</strong> category are:</p>

<ul>
{% for post in site.categories.dns %}
  {% if post.url %}
        <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>
