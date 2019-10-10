---
layout: page
title: Projects
permalink: /projects/
---

Here are the projects I've worked on! I'm still working on some interesting stuff so stay tuned!

<ul>
  {% for post in site.categories.projects %}
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