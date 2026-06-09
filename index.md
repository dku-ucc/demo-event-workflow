# DKU UCC Events

{% assign sorted_events = site.events | sort: 'date' | reverse %}
{% for event in sorted_events %}

## [{{ event.title }}]({{ event.url }})
📅 {{ event.date | date: "%B %d, %Y" }} | 📍 {{ event.location }}

{{ event.content | strip_html | truncate: 200 }}

[Read more →]({{ event.url }})

---
{% endfor %}
