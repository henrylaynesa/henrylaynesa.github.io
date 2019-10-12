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
	        <p class="post-meta">
		      <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">
		        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
		        {{ post.date | date: date_format }}
		      </time>
		      {% if post.author and post.show_author %}
		        • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ post.author }}</span></span>
		      {% endif %}
		      {% if post.tags and post.show_tags %}
		      	• 
		      	{% for tag in post.tags %}
		      		{% if tag != post.tags.first %}
		      			-
		      		{% endif %}
		      		<span itemprop="tag" itemscope itemtype="http://schema.org/Person"><span itemprop="name"><i>{{ tag }}</i></span></span>
		      	{% endfor %}
		      {% endif %}
		  	</p>
	        <meta name="description" content="{{ post.summary | escape }}">
	        <meta name="keywords" content="{{ post.tags | join: ', ' | escape }}"/>
	    </article>
    </li>
  {% endfor %}
</ul>