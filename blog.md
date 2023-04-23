---
layout: page
title: Blog
sidebar_sort_order: 1
---
{% include post-tags.html %}

{% assign posts = site.posts | where:"hide", "false" %}
{% for post in posts %}
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <div class="post-tags">
    {% for tag in post.tags %}
      {% if tags_page %}
      <a href="{{ site.baseurl }}{{ tags_page.url }}#{{ tag | slugify }}">
      {% else %}<span>{% endif %}
        <span class="icon">
          {% include svg/tags.svg %}
        </span>&nbsp;<span class="tag-name">{{ tag }}</span>
      {% if tags_page %}</a>{% else %}</span>{% endif %}
    {% endfor %}
  </div>
  <i> {{ post.date | date_to_string }} </i>
  <p>{{ post.excerpt }}</p>
  ---
{% endfor %}
