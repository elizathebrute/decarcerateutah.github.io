---
layout: default
nav: true
title: news | decarcerate utah
---

<div class="posts">
  {% for post in site.posts %} {% if post.news %}
    {% include post_excerpt.html %}
  {% endif %} {% endfor %}
</div>

