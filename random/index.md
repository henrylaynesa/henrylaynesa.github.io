---
layout: page
title: Random
permalink: /random/
---

Random thoughts and experiments to satisfy some curiosities. This is where I'll try to document specific lessons and insights I've picked up!

<ul>
  {% for post in site.categories.random %}
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