---
layout: page
permalink: /publications/
title: Publications
description: Selected publications in reverse chronological order. For the full list, see <a href='https://scholar.google.com/citations?user=2itcij4AAAAJ'>Dr. Zhao's Google Scholar</a>.
nav: true
nav_order: 5
---

<!-- _pages/publications.md -->

<!--
  JOURNAL SLIDESHOW: snapshots of first pages in assets/img/journals/.
  Format per slide: image | journal (year) | paper title | link ; slides separated by ";"
-->
{% capture journal_slides %}
nature-machine-intelligence-2026.jpg|Nature Machine Intelligence (2026)|Tensegrity continuum robots enable task-adaptive morphologies for cooperative behaviours|https://doi.org/10.1038/s42256-026-01335-4;
nature-communications-2023.jpg|Nature Communications (2023)|Embedded shape morphing for morphologically adaptive robots|https://doi.org/10.1038/s41467-023-41708-6;
science-advances-2020.jpg|Science Advances (2020)|Leveraging elastic instabilities for amplified performance|https://doi.org/10.1126/sciadv.aaz6912;
ieee-tro-2022.jpg|IEEE Transactions on Robotics (2022)|Physics-based modeling of twisted-and-coiled actuators using Cosserat rod theory|https://doi.org/10.1109/TRO.2021.3104238;
soft-robotics-2021.jpg|Soft Robotics (2021)|Twisted-and-coiled actuators with free strokes enable soft robots with programmable motions|https://doi.org/10.1089/soro.2019.0175;
ieee-tmech-2022.jpg|IEEE/ASME Transactions on Mechatronics (2022)|Origami-inspired modules enable a reconfigurable robot with programmable shapes and motions|https://doi.org/10.1109/TMECH.2022.3175145;
ieee-ral-2019.jpg|IEEE Robotics and Automation Letters (2019)|An adaptive walking robot with reconfigurable mechanisms using shape morphing joints|https://doi.org/10.1109/LRA.2019.2893439
{% endcapture %}
{% assign jslides = journal_slides | strip | split: ";" %}

<div class="lab-slideshow journal-show" aria-roledescription="carousel" aria-label="Highlighted journal publications">
  {% for s in jslides %}
    {% assign p = s | strip | split: "|" %}
    <figure class="lab-slide{% if forloop.first %} active{% endif %}" aria-hidden="{% if forloop.first %}false{% else %}true{% endif %}">
      <a href="{{ p[3] }}"><img src="{{ '/assets/img/journals/' | append: p[0] | relative_url }}" alt="First page of {{ p[2] }}, {{ p[1] }}" {% unless forloop.first %}loading="lazy"{% endunless %}></a>
      <figcaption><strong>{{ p[1] }}</strong> · <a href="{{ p[3] }}">{{ p[2] }}</a></figcaption>
    </figure>
  {% endfor %}
  <button class="lab-slide-btn prev" type="button" aria-label="Previous paper">&#10094;</button>
  <button class="lab-slide-btn next" type="button" aria-label="Next paper">&#10095;</button>
  <div class="lab-slide-dots">
    {% for s in jslides %}<button type="button" aria-label="Show paper {{ forloop.index }}"{% if forloop.first %} class="active"{% endif %}></button>{% endfor %}
  </div>
</div>

<script>
  (function () {
    var root = document.querySelector(".journal-show");
    if (!root) return;
    var slides = root.querySelectorAll(".lab-slide");
    var dots = root.querySelectorAll(".lab-slide-dots button");
    var reduce = window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches;
    var i = 0, timer = null;
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


<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>
