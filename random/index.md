---
layout: page
title: Random
permalink: /random/
---

Random thoughts and experiments to satisfy some curiosities.

<ul>
  {% for post in site.categories.random %}
    <li>
        <span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
        <meta name="description" content="{{ post.summary | escape }}">
        <meta name="keywords" content="{{ post.tags | join: ', ' | escape }}"/>
    </li>
  {% endfor %}
</ul>