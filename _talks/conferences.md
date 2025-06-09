---
title: Conferences
layout: page
permalink: /conferences/
---

{% assign conferences = site.talks | where: "event", "Conference" | sort: "date_start" | reverse %}

{% for conf in conferences %}
  {% assign start = conf.date_start | date: "%d %m %Y" %}
  {% assign end = conf.date_end | date: "%d %m %Y" %}
  - **[{{ conf.title }}]({{ conf.url }})**  
    📅 {{ start }}–{{ end }} | 📍 {{ conf.location }}
{% endfor %}
