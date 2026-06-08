# DKU UCC 活动列表

欢迎来到 DKU UCC 事件自动发布系统测试站。

{% for event in site.events %}
## [{{ event.title }}]({{ event.url }})
📅 {{ event.date | date: "%Y-%m-%d" }} | 📍 {{ event.location }}

{{ event.excerpt | strip_html | truncate: 100 }}

---
{% endfor %}
