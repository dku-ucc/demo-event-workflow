# DKU UCC Events

Welcome to the DKU UCC automatic event publishing system test site.

{% assign sorted_events = site.events | sort: 'date' | reverse %}
{% for event in sorted_events %}

## [{{ event.title }}]({{ event.url }})
📅 {{ event.date | date: "%B %d, %Y" }} | 📍 {{ event.location }}

{{ event.excerpt | strip_html | truncate: 120 }}

---
{% endfor %}
