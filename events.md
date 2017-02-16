---
layout: default
title: Upcoming Events
---


{% for event in site.events %}
  <h2>{{ event.title }}</h2>
  <p>{{ event.host }}{% if event.location %}, in  {{ event.location }}{% endif %} {% if event.time %} at {{event.time }} {% endif %}</p>

{% endfor %}