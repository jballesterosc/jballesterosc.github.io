---
layout: page
title: writing
permalink: /writing/
nav: true
nav_order: 4
pagination:
  enabled: true
  collection: posts
  permalink: /writing/page/:num/
  per_page: 20
  sort_field: date
  sort_reverse: true
  trail:
    before: 1
    after: 3
---

{% if page.pagination.enabled %}
  {% assign postlist = paginator.posts %}
{% else %}
  {% assign postlist = site.posts %}
{% endif %}

{% if postlist.size > 0 %}
<ul class="writing-list">
  {% for post in postlist %}
    <li>
      <span class="writing-date">{{ post.date | date: "%b %Y" }}</span>
      <a class="writing-title" href="{{ post.url | relative_url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
{% else %}
  <p class="writing-empty">Nothing here yet.</p>
{% endif %}

{% if page.pagination.enabled %}
{% include pagination.liquid %}
{% endif %}
