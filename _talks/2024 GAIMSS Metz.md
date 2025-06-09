---
title: Conferences
layout: page
permalink: /conferences/
---

## Conferences

{% for conf in site.data.conferences %}
  {% assign start_month_day = conf.date_start | date: "%b %d" %}
  {% assign end_day_year = conf.date_end | date: "%d, %Y" %}
  - **[{{ conf.title }}]({{ conf.url }})**  
    📅 {{ start_month_day }}–{{ end_day_year }} | 📍 {{ conf.location }}  
    {% if conf.notes %}*{{ conf.notes }}*{% endif %}
{% endfor %}
