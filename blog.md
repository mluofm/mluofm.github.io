---
title: Blog
permalink: /blog/
layout: page
---

# Blog

<div class="list-group">
  {% for post in site.posts %}
  <a href="{{ post.url }}" class="list-group-item list-group-item-action">
    <div class="d-flex w-100 justify-content-between">
      <h5 class="mb-1">{{ post.title }}</h5>
      {% if post.author.name %}<small>By {{ post.author.name }}</small>{% endif %}
    </div>
    {% if post.short_description %}<p class="mb-1">{{ post.short_description }}</p>{% endif %}
    <small>{% for category in post.categories %} {{ category }} {% endfor %}</small>
  </a>
  {% endfor %}
</div>