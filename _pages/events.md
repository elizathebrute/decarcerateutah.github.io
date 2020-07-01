---
layout: page
title: events | decarcerate utah
nav: true
position: 2
permalink: /events/
---

{% assign events = site.pages | where: "event", "true" | reverse %}
<div class="events">
  {% assign node = events | first %}
  {% assign other_events = events | shift %}

  {% include event.html is_first="true" %}

  {% for node in other_events %}
    {% include event.html %}
  {% endfor %}
</div>
