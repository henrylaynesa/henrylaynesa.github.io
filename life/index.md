---
layout: page
title: Life
permalink: /life/
---

Reflections and realizations on some of the things I've encountered in my career.

<ul>
  {% for post in site.categories.life %}
    <li>
        <article>
        	<h3><a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h3>
	        <p><h5>{{ post.date | date_to_string }}</h5></p>
	        <meta name="description" content="{{ post.summary | escape }}">
	        <meta name="keywords" content="{{ post.tags | join: ', ' | escape }}"/>
	    </article>
    </li>
  {% endfor %}
</ul>