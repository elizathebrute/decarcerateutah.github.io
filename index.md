---
layout: default
title: news | decarcerate utah
---

{% assign featured = site.posts | where: "featured", "true" %}

{% if featured.size > 0 %}
  {% assign featured_post = featured.first %}
{% else %}
  {% assign featured_post = site.posts.first %}
{% endif %}

{% assign post = featured.first %}
<div class="post-featured">
  {% include post_teaser.html %}
</div>

<div class="posts">
  {% assign other_posts = site.posts | where_exp: "item", "item.title != featured_post.title" %}
  {% for post in other_posts limit: 4 %}
    <div class="post-teaser">
      {% include post_teaser.html %}
    </div>
  {% endfor %}
</div>

<div class="all-posts">
  <h3><a href="/posts/">see all posts</a></h3>
</div>

