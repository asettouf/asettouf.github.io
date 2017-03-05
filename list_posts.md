---
layout: page
title: Articles
additional_info: List of articles I wrote
permalink: /articles/
order: 3
---
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>