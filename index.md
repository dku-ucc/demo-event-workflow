---
layout: home
title: DKU UCC Events
---

{% assign sorted_events = site.pages | where: "type", "event" | sort: "date" | reverse %}

{% for event in sorted_events %}
<article class="event-card">
  <h2>
    <a href="{{ event.url | relative_url }}">{{ event.title }}</a>
  </h2>

  <p class="meta">
    📅 {{ event.date | date: "%B %d, %Y" }}
    {% if event.location %} | 📍 {{ event.location }}{% endif %}
  </p>

  {% if event.poster %}
    <img class="thumbnail" src="{{ event.url | relative_url }}{{ event.poster }}" alt="{{ event.title }} poster">
  {% endif %}

  <p>{{ event.content | strip_html | truncate: 200 }}</p>

  <p><a href="{{ event.url | relative_url }}">Read more →</a></p>
</article>
{% endfor %}
