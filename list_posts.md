---
layout: page
title: Articles
additional_info: List of articles I wrote
permalink: /articles/
order: 3
---
<ul class="post-list">
  {% for post in site.posts %}
    <li>
      <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

      <h2>
        <a class="post-link" href="{{ post.url | relative_url }}"
        data-disqus-identifier="{{ post.date | date: "%b %-d, %Y" }}">
          {{ post.title | escape }}</a>
          <a class="comment-counts" href="{{ post.url | relative_url }}#disqus_thread"></a>
      </h2>
    </li>
  {% endfor %}
</ul>
