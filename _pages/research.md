---
layout: page
title: Research
permalink: /research/
description: To create adaptive robots, we leverage mechanical and biological principles, novel materials, and dynamic control to guide our design.
nav: true
nav_order: 3
---

<a href="{{ '/assets/img/research/research-overview.jpg' | relative_url }}"><img class="img-fluid rounded z-depth-1 mb-4" src="{{ '/assets/img/research/research-overview.jpg' | relative_url }}" alt="Research overview: adaptive mechanisms (tensegrity, linkages, origami, bistable structures, morphing modules, soft systems), enabled by artificial muscles, variable-stiffness joints, and shape-memory alloys, build perching, origami, tensegrity, fish-like, and multimodal robots for search and rescue, infrastructure inspection, space exploration, and environmental monitoring"></a>

Our research spans four connected areas. Click an area to see what we study, key results, and the related robots and papers.

<!--
  Each research area is one Markdown file in the _areas/ folder.
  Papers appear on an area page automatically when their entry in
  _bibliography/papers.bib has `area = {...}` containing that area's key.
-->

{% assign areas = site.areas | sort: "order" %}

<div class="row robot-grid mt-4">
  {% for area in areas %}
    <div class="col-sm-6 mb-4">
      <a href="{{ area.url | relative_url }}" class="robot-card-link">
        <div class="card h-100 hoverable">
          {% if area.card_video %}
            <video
              class="card-img-top"
              src="{{ area.card_video | relative_url }}"
              poster="{{ area.img | relative_url }}"
              autoplay
              loop
              muted
              playsinline
              aria-label="{{ area.title }}"
            ></video>
          {% else %}
            <img class="card-img-top" src="{{ area.img | relative_url }}" alt="{{ area.title }}" loading="lazy">
          {% endif %}
          <div class="card-body">
            <h2 class="card-title">{{ area.title }}</h2>
            <p class="card-text">{{ area.description }}</p>
          </div>
        </div>
      </a>
    </div>
  {% endfor %}
</div>

## Research support

Our research is supported by the National Science Foundation (NSF), DARPA, the Colorado Office of Economic Development and International Trade (OEDIT), and the Center for Transformative Infrastructure Preservation and Sustainability (CTIPS).

<div class="sponsor-logos">
  <a href="https://www.nsf.gov" title="U.S. National Science Foundation"><img class="seal" src="{{ '/assets/img/sponsors/nsf.png' | relative_url }}" alt="U.S. National Science Foundation" loading="lazy"></a>
  <a href="https://www.darpa.mil/work-with-us/communities/small-business/sbir-sttr-overview" title="DARPA Small Business Technology Transfer (STTR)"><img src="{{ '/assets/img/sponsors/darpa-sttr.png' | relative_url }}" alt="DARPA Small Business Technology Transfer (STTR)" loading="lazy"></a>
  <a href="https://oedit.colorado.gov" title="Colorado Office of Economic Development and International Trade"><img class="tall" src="{{ '/assets/img/sponsors/oedit.png' | relative_url }}" alt="Colorado Office of Economic Development and International Trade (OEDIT)" loading="lazy"></a>
  <a href="https://www.ctips.org" title="Center for Transformative Infrastructure Preservation and Sustainability"><img src="{{ '/assets/img/sponsors/ctips.png' | relative_url }}" alt="CTIPS: Center for Transformative Infrastructure Preservation and Sustainability, USDOT Region 8 University Transportation Center" loading="lazy"></a>
</div>
