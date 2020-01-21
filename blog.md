---
layout: page
title: Blog
---

{% for post in site.posts %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <i> {{ post.date | date_to_string }} </i>
  <p>{{ post.excerpt }}</p>
  ---
{% endfor %}
