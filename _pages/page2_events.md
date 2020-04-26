---
layout: page
title: events | decarcerate utah
nav: true
permalink: /events/
---

<div class="events">
  {% for node in site.pages %} {% if node.event %}
    {% include event.html %}
  {% endif %} {% endfor %}
</div>

