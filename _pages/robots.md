---
layout: page
title: Robots
permalink: /robots/
description: Robots developed in the Adaptive Robotics Lab. Click a robot to see how it works and what it can do.
nav: true
nav_order: 4
---

<!--
  Each robot is one Markdown file in the _robots/ folder (see _robots/tecobot.md).
  Cards are sorted by the `order` field (smallest first), then by title.
  The card shows `card_video` (a short muted .mp4 loop) if given, otherwise `img`.
-->

{% assign robots = site.robots | sort: "order" %}

<div class="row robot-grid">
  {% for robot in robots %}
    <div class="col-sm-6 col-lg-4 mb-4">
      <a href="{{ robot.url | relative_url }}" class="robot-card-link">
        <div class="card h-100 hoverable">
          {% if robot.card_video %}
            <video
              class="card-img-top"
              src="{{ robot.card_video | relative_url }}"
              poster="{{ robot.img | relative_url }}"
              autoplay
              loop
              muted
              playsinline
              aria-label="{{ robot.title }}"
            ></video>
          {% elsif robot.img %}
            <img class="card-img-top" src="{{ robot.img | relative_url }}" alt="{{ robot.title }}" loading="lazy">
          {% endif %}
          <div class="card-body">
            <h2 class="card-title">{{ robot.title }}</h2>
            <p class="card-text">{{ robot.description }}</p>
            {% if robot.year %}
              <p class="card-text"><small class="text-muted">{{ robot.year }}{% if robot.venue %} · {{ robot.venue }}{% endif %}</small></p>
            {% endif %}
          </div>
        </div>
      </a>
    </div>
  {% endfor %}
</div>
