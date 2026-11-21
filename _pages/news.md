---
layout: page
title: news
nav: true
nav_order: 1
permalink: /news/
---

<!-- Each news item's picture comes from `image:` in its front matter (_news/*.md); add `image_fit: contain` for logos. -->
<div class="news-list">
  {% assign news_items = site.news | reverse %}
  {% for item in news_items %}
    <div class="news-item">
      <div class="news-thumb{% if item.image_fit == 'contain' %} news-thumb-logo{% endif %}">
        {% if item.image %}<img src="{{ item.image | relative_url }}" alt="" loading="lazy">{% endif %}
      </div>
      <div class="news-body">
        <div class="news-date">{{ item.date | date: '%b %d, %Y' }}</div>
        {% if item.inline %}
          {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
        {% else %}
          <a class="news-title" href="{{ item.url | relative_url }}">{{ item.title }}</a>
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>
