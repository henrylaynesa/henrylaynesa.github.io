---
layout: page
title: Life
permalink: /life/
---

Reflections and realizations on some of the things I've encountered in my career.

<ul>
  {% for post in site.categories.life %}
    <li>
        <span>{{ post.date | date_to_string }}</span> » <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
        <meta name="description" content="{{ post.summary | escape }}">
        <meta name="keywords" content="{{ post.tags | join: ', ' | escape }}"/>
    </li>
  {% endfor %}
</ul>