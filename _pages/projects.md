---
layout: page
title: projects
permalink: /projects/
description: A few personal projects and things I've built.
nav: true
nav_order: 2
---

<!-- pages/projects.md -->
{% assign sorted_projects = site.projects | sort: "importance" %}

<ul class="project-list">
  {% for project in sorted_projects %}
    <li>
      <a class="project-row" href="{% if project.redirect %}{{ project.redirect }}{% else %}{{ project.url | relative_url }}{% endif %}">
        <div class="project-row-header">
          <span class="project-title">{{ project.title }}</span>
          {% if project.timeframe %}<span class="project-timeframe">{{ project.timeframe }}</span>{% endif %}
        </div>
        <p class="project-description">{{ project.description }}</p>
      </a>
      {% if project.github %}
        <a class="project-code-link" href="{{ project.github }}" target="_blank" rel="noopener">code</a>
      {% endif %}
    </li>
  {% endfor %}
</ul>
