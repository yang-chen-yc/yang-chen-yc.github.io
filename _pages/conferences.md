---
layout: page
title: Conferences
permalink: /conferences/
---

Here is a list of conferences I've attended:

<ul>
{% for conference in site.conferences %}
  <li>
    <strong>{{ conference.title }}</strong> - {{ conference.conference }} ({{ conference.date | date: "%Y" }})
    {% if conference.location %} - {{ conference.location }}{% endif %}
  </li>
{% endfor %}
</ul>
