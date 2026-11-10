---
layout: default
title: Blog
permalink: /blog/
---

# Blog

{% if site.posts.size == 0 %}
<p class="muted">No posts yet.</p>
{% else %}
<ul class="posts">
{% for post in site.posts %}
  <li dir="{% if post.lang == 'ar' %}rtl{% else %}ltr{% endif %}">
    <span class="muted">{{ post.date | date: "%Y-%m-%d" }}</span> ·
    <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
  </li>
{% endfor %}
</ul>
{% endif %}
