---
layout: default
title: Posts
---
# Latest Posts

<ul>
  {% for post in site.posts %}
    <li>
      <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
      <span class="text-muted pull-right">{{ post.date | date_to_string }}</span>
      <p>{{ post.excerpt | strip_html }}</p>
    </li>
    <hr>
  {% endfor %}
</ul>
