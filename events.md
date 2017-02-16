---
layout: default
title: Upcoming Events
---


{% for event in site.events %}
  <h2>{{ event.title }}</h2>
  <p>Performed by {{ event.artist }}{% if event.director %}, directed by {{ event.director }}{% endif %}</p>
  {% for work in director.works %}
    <h3>{{ work.title }}</h3>
    <p>Composed by {{ work.composer }}</p>
    <ul>
    {% for track in work.tracks %}
      <li>{{ track.title }} ({{ track.duration }})</li>
    {% endfor %}
    </ul>
  {% endfor %}
{% endfor %}