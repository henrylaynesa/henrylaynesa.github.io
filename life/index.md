---
layout: page
title: Life
permalink: /life/
---

Reflections and realizations on my personal milestones with some storytelling and a sprinkle of opinions.

<ul>
  {% for post in site.categories.life %}
    <li>
        <article>
        	<h3><a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></h3>
	        <p class="post-meta">
		      <time datetime="{{ post.date | date_to_xmlschema }}" itemprop="datePublished">
		        {% assign date_format = site.minima.date_format | default: "%b %-d, %Y" %}
		        {{ post.date | date: date_format }}
		      </time>
		      {% if post.author %}
		        • <span itemprop="author" itemscope itemtype="http://schema.org/Person"><span itemprop="name">{{ post.author }}</span></span>
		      {% endif %}
		  	</p>
	        <meta name="description" content="{{ post.summary | escape }}">
	        <meta name="keywords" content="{{ post.tags | join: ', ' | escape }}"/>
	    </article>
    </li>
  {% endfor %}
</ul>