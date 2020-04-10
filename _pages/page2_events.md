---
layout: page
title: events | decarcerate utah
nav: true
permalink: /events/
---

<div class="events">
  {% for post in site.posts %} {% if post.event %}
    {{ post.content }}
  {% endif %} {% endfor %}
</div>

