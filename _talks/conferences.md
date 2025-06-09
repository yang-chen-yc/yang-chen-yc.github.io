---
title: Conferences
layout: page
permalink: /conferences/
---

{% assign conferences = site.talks | where: "event", "Conference" | sort: "date_start" | reverse %}

{% for conf in conferences %}
  {% assign start_date = conf.date_start | date: "%d %B %Y" %}
  {% assign end_date = conf.date_end | date: "%d %B %Y" %}
  - **[{{ conf.title }}]({{ conf.url }})**  
    🗓️ {% if conf.date_start == conf.date_end %}
      {{ start_date }}
    {% else %}
      {{ start_date }} – {{ end_date }}
    {% endif %} | 📍 {{ conf.location }}
{% endfor %}
