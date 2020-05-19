---
layout: default
permalink: /posts/
title: news | decarcerate utah
---

<div class="posts">
  <div class="empty-top"></div>
  {% for post in site.posts %}
    {% include post_teaser.html %}
  {% endfor %}
  <div class="empty-bottom"></div>
</div>

