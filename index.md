---
layout: default
nav: true
title: news | decarcerate utah
---

<div class="posts">
  {% for post in site.posts %}
    {% include post_excerpt.html %}
  {% endfor %}
</div>

