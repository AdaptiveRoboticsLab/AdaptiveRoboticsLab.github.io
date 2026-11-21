---
layout: about
title: About
permalink: /

# News and selected papers are placed inside the page content below (so "Join us" can come last),
# so the theme's built-in sections are turned off here. `limit` is still read by news.liquid.
selected_papers: false
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false
  scrollable: false
  limit: 4

latest_posts:
  enabled: false
---

<!--
  HERO SLIDESHOW: each slide is a short, muted, looping .mp4 plus a caption that links to a page.
  Edit the list below to change clips. Only the visible clip is downloaded.
  Format per slide: video | poster image | caption | link
-->

{% capture hero_slides %}
/assets/video/robots/tecobot/card.mp4|/assets/img/robots/tecobot/card.jpg|TeCoBot: soft robots that link up into new shapes|/robots/tecobot/;
/assets/video/robots/shape-morphing/smart-river.mp4|/assets/video/robots/shape-morphing/smart-river.jpg|SMART: an amphibious robot that turns flippers into legs|/robots/shape-morphing/;
/assets/video/robots/tensegrity-wheels/overview.mp4|/assets/video/robots/tensegrity-wheels/overview.jpg|A robot that rolls on tensegrity wheels and jumps over obstacles|/robots/tensegrity-wheels/;
/assets/video/research/hybrid-perching.mp4|/assets/video/research/hybrid-perching.jpg|Drones that perch on branches and walls to save energy|/research/aerial-robots/;
/assets/video/robots/origami/gait-switch.mp4|/assets/video/robots/origami/gait-switch.jpg|An origami robot that changes its gait by heating one joint|/robots/origami-robot/
{% endcapture %}
{% assign slides = hero_slides | strip | split: ";" %}

<div class="lab-hero-video lab-slideshow" aria-roledescription="carousel" aria-label="Robots from the Adaptive Robotics Lab">
  {% for s in slides %}
    {% assign p = s | strip | split: "|" %}
    <figure class="lab-slide{% if forloop.first %} active{% endif %}" aria-hidden="{% if forloop.first %}false{% else %}true{% endif %}">
      <video
        src="{{ p[0] | relative_url }}"
        poster="{{ p[1] | relative_url }}"
        muted
        loop
        playsinline
        preload="{% if forloop.first %}auto{% else %}none{% endif %}"
        {% if forloop.first %}autoplay{% endif %}
      ></video>
      <figcaption><a href="{{ p[3] | relative_url }}">{{ p[2] }} &rarr;</a></figcaption>
    </figure>
  {% endfor %}
  <div class="lab-hero-text">
    <h1>Adaptive Robotics Lab</h1>
    <p>Department of Mechanical Engineering · Colorado State University</p>
  </div>
  <button class="lab-slide-btn prev" type="button" aria-label="Previous video">&#10094;</button>
  <button class="lab-slide-btn next" type="button" aria-label="Next video">&#10095;</button>
  <div class="lab-slide-dots">
    {% for s in slides %}<button type="button" aria-label="Show video {{ forloop.index }}"{% if forloop.first %} class="active"{% endif %}></button>{% endfor %}
  </div>
</div>

<script>
  (function () {
    var root = document.querySelector(".lab-hero-video");
    if (!root) return;
    var slides = root.querySelectorAll(".lab-slide");
    var dots = root.querySelectorAll(".lab-slide-dots button");
    var reduce = window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    var i = 0, timer = null;
    function video(k) { return slides[k].querySelector("video"); }
    function show(n) {
      var old = video(i);
      slides[i].classList.remove("active"); slides[i].setAttribute("aria-hidden", "true"); dots[i].classList.remove("active");
      if (old) old.pause();
      i = (n + slides.length) % slides.length;
      slides[i].classList.add("active"); slides[i].setAttribute("aria-hidden", "false"); dots[i].classList.add("active");
      var v = video(i);
      if (v && !reduce) { v.currentTime = 0; var pr = v.play(); if (pr && pr.catch) pr.catch(function () {}); }
    }
    function start() { if (!reduce) { stop(); timer = setInterval(function () { show(i + 1); }, 8000); } }
    function stop() { if (timer) { clearInterval(timer); timer = null; } }
    if (reduce) { var v0 = video(0); if (v0) { v0.removeAttribute("autoplay"); v0.pause(); } }
    root.querySelector(".prev").addEventListener("click", function () { show(i - 1); start(); });
    root.querySelector(".next").addEventListener("click", function () { show(i + 1); start(); });
    dots.forEach(function (d, k) { d.addEventListener("click", function () { show(k); start(); }); });
    root.addEventListener("mouseenter", stop);
    root.addEventListener("mouseleave", start);
    start();
  })();
</script>

The **Adaptive Robotics Lab** at Colorado State University designs and builds small robots that adapt to new tasks and environments by changing their shape, stiffness, structure, or way of moving. We combine soft materials, reconfigurable mechanisms, and bio-inspired design with modeling and control, with applications in search and rescue, infrastructure inspection, space exploration, and environmental monitoring. The lab is directed by Prof. [Jianguo Zhao]({{ '/people/' | relative_url }}) and is located at the Powerhouse Energy Campus in Fort Collins, Colorado.

## Research areas

{% assign areas = site.areas | sort: "order" %}
<div class="row robot-grid home-cards">
  {% for area in areas %}
    <div class="col-6 col-md-3 mb-3">
      <a href="{{ area.url | relative_url }}" class="robot-card-link">
        <div class="card h-100 hoverable">
          <img class="card-img-top" src="{{ area.img | relative_url }}" alt="{{ area.title }}" loading="lazy">
          <div class="card-body">
            <h3 class="card-title">{{ area.title }}</h3>
          </div>
        </div>
      </a>
    </div>
  {% endfor %}
</div>

## [News]({{ '/news/' | relative_url }})

<div class="news-list">
  {% assign news_items = site.news | reverse %}
  {% for item in news_items limit: 4 %}
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

## [Selected publications]({{ '/publications/' | relative_url }})

{% include selected_papers.liquid %}

<div class="lab-callout">
  <h2>Join us</h2>
  <p>We are always looking for motivated graduate and undergraduate students interested in robotics, controls, mechanical design, mechatronics, and embedded systems. Please email <a href="mailto:Jianguo.Zhao@colostate.edu">Prof. Zhao</a> with your CV, or search "Adaptive Robotics Laboratory" at <a href="https://jobs.colostate.edu">jobs.colostate.edu</a>. We also welcome collaborations with industry partners.</p>
</div>
