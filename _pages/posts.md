---
layout: default
nav: true
permalink: /posts/
title: news | decarcerate utah
---

<div class="posts">
  {% for post in site.posts %}
    {% include post_teaser.html %}
  {% endfor %}
</div>

