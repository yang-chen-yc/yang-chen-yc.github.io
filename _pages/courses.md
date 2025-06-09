---
layout: archive
title: "Advanced Courses"
permalink: /courses/
---

{% assign courses = site.advancedcourses | sort: "date_start" | reverse %}

<div class="entries-list">
  {% for post in courses %}
    <div class="course-item">
      <h3 class="course-title">{{ post.title }}</h3>
      <div class="course-meta">
        <strong>{{ post.course }}</strong>. 
        {{ post.date_start | date: "%d %B %Y" }}
        {% if post.date_end %}– {{ post.date_end | date: "%d %B %Y" }}{% endif %}
        {% if post.venue %} | {{ post.venue }}{% endif %}
        {% if post.location %} | {{ post.location }}{% endif %}
      </div>
    </div>
  {% endfor %}
</div>
