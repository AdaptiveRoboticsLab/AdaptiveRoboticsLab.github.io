---
layout: page
title: People
permalink: /people/
description: members of the Adaptive Robotics Lab
nav: true
nav_order: 2
---

<!-- Slideshow: add/remove photos in the list below (3:2 images in assets/img/lab/slides/). -->
{% assign slides = "lunch-2025-12|Lab lunch, December 2025;lunch-2024-08|Lab lunch, August 2024;defense-eli|Elisha Lerner's Ph.D. defense;defense-andrew|Andrew Stefka's M.S. defense, October 2026;defense-bryce|Bryce Jones's M.S. defense, August 2024;icra-2022-jiefeng|Jiefeng Sun presenting at ICRA 2022;senior-design-josh|Josh Chrisler presenting his senior design project, April 2025" | split: ";" %}
<div class="lab-slideshow" aria-roledescription="carousel" aria-label="Lab activities">
  {% for s in slides %}
    {% assign parts = s | split: "|" %}
    <figure class="lab-slide{% if forloop.first %} active{% endif %}" aria-hidden="{% if forloop.first %}false{% else %}true{% endif %}">
      <img src="{{ '/assets/img/lab/slides/' | append: parts[0] | append: '.jpg' | relative_url }}" alt="{{ parts[1] }}" {% unless forloop.first %}loading="lazy"{% endunless %}>
      <figcaption>{{ parts[1] }}</figcaption>
    </figure>
  {% endfor %}
  <button class="lab-slide-btn prev" type="button" aria-label="Previous photo">&#10094;</button>
  <button class="lab-slide-btn next" type="button" aria-label="Next photo">&#10095;</button>
  <div class="lab-slide-dots">
    {% for s in slides %}<button type="button" aria-label="Show photo {{ forloop.index }}"{% if forloop.first %} class="active"{% endif %}></button>{% endfor %}
  </div>
</div>

<script>
  (function () {
    var root = document.querySelector(".lab-slideshow");
    if (!root) return;
    var slides = root.querySelectorAll(".lab-slide");
    var dots = root.querySelectorAll(".lab-slide-dots button");
    var i = 0, timer = null;
    var reduce = window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    function show(n) {
      slides[i].classList.remove("active"); slides[i].setAttribute("aria-hidden", "true"); dots[i].classList.remove("active");
      i = (n + slides.length) % slides.length;
      slides[i].classList.add("active"); slides[i].setAttribute("aria-hidden", "false"); dots[i].classList.add("active");
    }
    function start() { if (!reduce) { stop(); timer = setInterval(function () { show(i + 1); }, 5000); } }
    function stop() { if (timer) { clearInterval(timer); timer = null; } }
    root.querySelector(".prev").addEventListener("click", function () { show(i - 1); start(); });
    root.querySelector(".next").addEventListener("click", function () { show(i + 1); start(); });
    dots.forEach(function (d, k) { d.addEventListener("click", function () { show(k); start(); }); });
    root.addEventListener("mouseenter", stop);
    root.addEventListener("mouseleave", start);
    start();
  })();
</script>

## Lab Director

<div class="director">
  <img class="director-photo" src="{{ '/assets/img/people/jianguo-zhao.jpg' | relative_url }}" alt="Dr. Jianguo Zhao">
  <div markdown="1">
**Dr. Jianguo Zhao** is an Associate Professor in the Department of Mechanical Engineering at Colorado State University, where he has directed the Adaptive Robotics Lab since 2015. His research on robot design, modeling, and control is supported mainly by the National Science Foundation and has appeared in robotics journals such as IEEE Transactions on Robotics and Soft Robotics, as well as multidisciplinary journals including Nature Machine Intelligence, Nature Communications, and Science Advances. He has served as a Technical Editor for IEEE/ASME Transactions on Mechatronics and an Associate Editor for IEEE Transactions on Robotics. He received his Ph.D. in Electrical Engineering from Michigan State University (2015), and his M.E. (2007) and B.E. (2005) from Harbin Institute of Technology, China.

Personal website: [jianguozhaorobotics.github.io](https://jianguozhaorobotics.github.io/) · [Google Scholar](https://scholar.google.com/citations?user=2itcij4AAAAJ&hl=en)

Email: [Jianguo.Zhao@colostate.edu](mailto:Jianguo.Zhao@colostate.edu) · Phone: 970-491-5927
  </div>
</div>

<!-- Current members come from _data/members.yml (photo, short text, and links for each person).
     Cards are shown postdocs first, then graduate students, then undergraduates. -->

## Current Members

<div class="row member-grid">
  {% assign groups = "postdoc,graduate,undergraduate" | split: "," %}
  {% for g in groups %}
    {% assign members = site.data.members | where: "group", g %}
    {% for m in members %}
      <div class="col-6 col-md-4 col-lg-3 mb-4">
        <div class="member-card">
          {% if m.photo %}
            <img class="member-photo" src="{{ m.photo | relative_url }}" alt="{{ m.name }}" loading="lazy">
          {% else %}
            <img class="member-photo member-photo-logo" src="{{ '/assets/img/people/csu-ram-symbol.png' | relative_url }}" alt="Colorado State University ram symbol" loading="lazy">
          {% endif %}
          <div class="member-name">{{ m.name }}</div>
          <div class="member-meta">{{ m.degree }}{% if m.since %}, since {{ m.since }}{% endif %}</div>
          {% if m.text %}<p class="member-text">{{ m.text }}</p>{% endif %}
          <div class="member-links">
            {% if m.website %}<a href="{{ m.website }}" title="Website"><i class="fa-solid fa-globe"></i></a>{% endif %}
            {% if m.scholar %}<a href="{{ m.scholar }}" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>{% endif %}
            {% if m.linkedin %}<a href="{{ m.linkedin }}" title="LinkedIn"><i class="fa-brands fa-linkedin"></i></a>{% endif %}
            {% if m.github %}<a href="{{ m.github }}" title="GitHub"><i class="fa-brands fa-github"></i></a>{% endif %}
          </div>
        </div>
      </div>
    {% endfor %}
  {% endfor %}
</div>

## Alumni

**Ph.D.**

- Elisha Lerner, Ph.D. ME, Summer 2026. Thesis: _Enabling Physically Intelligent Robots through Stiffness Tuning_
- Zhe Chen, Ph.D. ME, Fall 2025. Thesis: _Modular Reconfigurable Robots Capable of Programmable Shapes and Motions_
- Jiefeng Sun, Ph.D. ME, Summer 2022. Now Assistant Professor, Arizona State University
- Haijie Zhang, Ph.D. ME, Fall 2020. Now Data Scientist, Optum

**M.S. and M.E.**

- Andrew Stefka, M.S. ME, Fall 2026. Thesis: _Driving, Flying, Swimming, and Perching Robot_
- Josh Chrisler, M.S. ME, Fall 2026. Thesis: _Transformable Wheel-legged Robots_
- Clint Middlemist, M.S. ME, Fall 2024
- Bryce Jones, M.S. ME, Summer 2024. Now Testing Engineer, Blue Origin
- Ajai Singh, M.S. EE, Spring 2023. Now Control Engineer, Caterpillar
- Brandon Tighe, M.S. ME, Spring 2022. Now Manufacturing Engineer, Nordson Medical
- Billy Hsiao, M.S. EE, Fall 2021
- Ben Pawlowski, M.S. ME, Fall 2019
- Ali Abbas, M.S. ME, Spring 2018. Now System Engineer, Samsung
- Tony DeMario, M.S. ME, Summer 2018. Now President, Heath Steel
- Fei Jiang, M.E. ME, Summer 2016. Now Dimensional Engineer, Meta

**Undergraduate and visiting**

- Sydney Spiegel (B.S. ME, 2024), Heaven Smith (B.S. ME, 2021), Jordan Julian (B.S. ME, 2019), Jeff Larchar (B.S. ME, 2019), Bradley Pospeck (B.S. ME, 2018), David Trinko (B.S. ME, 2017), Jeffrey Gier (B.S. ME, 2016)
- Other undergraduate researchers: Mason Daly (B.S., Spring 2026), Alex Leadbetter (2024–2025), Jerry Lu (2024), Quincy Humphrey (2024), Anisha Kalla (2023–2024), Walter Jordan (2022–2023), Sebastian Mettes (2019)
- REU students: Alyssa Fournier (2024), Jacob Brannon (2023), Nick Woolsey (2022), Ben Burdess (2021), Simon Hempel-Costello (2021, 2022)
- High school: Feiyu Wu, Poudre High School (2020–2023)

## Lab Life

<div class="row">
  <div class="col-sm-4 mt-3"><img class="lab-thumb rounded z-depth-1" src="{{ '/assets/img/lab/lab-team.jpg' | relative_url }}" alt="Lab members with a small flying robot" loading="lazy"></div>
  <div class="col-sm-4 mt-3"><img class="lab-thumb rounded z-depth-1" src="{{ '/assets/img/lab/showcase.jpg' | relative_url }}" alt="Presenting the lab's robots at a campus event" loading="lazy"></div>
  <div class="col-sm-4 mt-3"><img class="lab-thumb rounded z-depth-1" src="{{ '/assets/img/lab/truss-robot.jpg' | relative_url }}" alt="Testing a legged robot built from modular truss legs" loading="lazy"></div>
</div>
