---
layout: default
title: news | decarcerate utah
---

<h1>Featured and Recent</h1>
<div class="posts">
  {% assign featured = site.posts | where: "featured", "true" %}

  {% if featured.size > 0 %}
    {% assign other_posts = site.posts | where_exp: "item", "item.title != featured.first.title" %}

    {% assign post = featured.first %}
    <div class="featured">
      {% include post_teaser.html %}
    </div>

    {% for post in other_posts limit:5 %}
      {% include post_teaser.html %}
    {% endfor %}
  {% else %}
    {% for post in site.posts limit: 6 %}
      {% include post_teaser.html %}
    {% endfor %}
  {% endif %}
</div>

<div class="all-posts">
  <h3><a href="/posts/">see all posts</a></h3>
</div>

