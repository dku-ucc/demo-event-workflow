---
layout: home
title: DKU UCC Events
---

## Introduction

Duke Kunshan University (DKU) University Colloquium aims to cultivate intellectual conversations across boundaries. Our colloquium committee selects pioneers of diverse backgrounds from academia, industry, government, NPO (Non-profit organizations), and beyond.

Our audience is university-wide, including undergraduate students, graduate students, researchers, faculty, and staff across disciplines and backgrounds. Therefore, a talk aimed at an intelligent but general audience will be most effective.

## Events

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
