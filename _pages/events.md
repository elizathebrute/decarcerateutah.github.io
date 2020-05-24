---
layout: page
title: events | decarcerate utah
nav: true
position: 2
permalink: /events/
---

{% assign events = site.pages | where: "event", "true" | reverse %}
<div class="events">
  <div class="empty-top"></div>
  {% for node in events %}
    {% include event.html %}
  {% endfor %}
  <div class="empty-bottom"></div>
</div>

