---
layout: page
title: events | decarcerate utah
nav: true
position: 2
permalink: /events/
---

<button class="calendar-button" onClick="toggleContent('calendar')">view calendar</button>
<div id="calendar" style="display: none;">
  <iframe
    src="https://teamup.com/ks1owsgwon9opdb4gn?showLogo=0&showSearch=0&showProfileAndInfo=0&showSidepanel=0&disableSidepanel=0&showTitle=0&showViewSelector=0&showMenu=0&showAgendaHeader=1&showAgendaDetails=0&showYearViewHeader=1"
    width="100%"
    height="500px"
    frameborder="0"
  ></iframe>
</div>

{% assign events = site.pages | where: "event", "true" | reverse %}
<div class="events">
  {% for node in events %}
    {% include event.html %}
  {% endfor %}
</div>

<script>
function toggleContent(id) {
  const element = document.getElementById(id);
  if (element.style) {
    if (element.style.display == 'block') {
      element.style.display = 'none';
    } else {
      element.style.display = 'block';
    }
  }
}
</script>
