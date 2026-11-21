---
layout: page
title: Multimodal Robots
description: Small robots that move in more than one way, rolling, jumping, walking, climbing, and swimming, to cross terrain no single mode can handle.
img: assets/img/robots/tensegrity-wheels/card.jpg
card_video: assets/video/robots/tensegrity-wheels/card.mp4
order: 4
area_key: multimodal
---

<video class="lab-media rounded z-depth-1 mb-3" src="{{ '/assets/video/robots/tensegrity-wheels/overview.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/overview.jpg' | relative_url }}" autoplay loop muted playsinline></video>

Animals switch between walking, running, jumping, climbing, and swimming as the terrain changes. Most robots can do only one of these. We build small robots that combine several ways of moving, so they can cross rubble, steps, gaps, sand, snow, and water, which matters for search and rescue, inspection, and exploration.

## Questions we work on

- **Combining modes in a small body.** How can a lightweight robot wheel and jump, or walk and climb, without carrying a separate mechanism for each mode?
- **Robust bodies.** Can compliant structures such as tensegrity wheels and soft joints absorb impacts and help a small robot survive falls?
- **Control in the air.** How can a jumping robot use a tail to control its body angle in mid-air and land safely?

## Key results

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/obstacle-course.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/obstacle-course.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Tensegrity wheels and a bistable jumper.</strong> The robot crosses an obstacle course of rocks, a wall, a pipe, a gap, a step, and a slope (2× speed).</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/tailbot.mp4' | relative_url }}" poster="{{ '/assets/video/research/tailbot.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>MSU Tailbot.</strong> A 26-gram robot that runs, jumps up steps, and uses its tail to steer in the air.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/miniwalker.mp4' | relative_url }}" poster="{{ '/assets/video/research/miniwalker.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>MiniWalker.</strong> A multi-material 3D-printed walking robot with soft joints and links.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/single.mp4' | relative_url }}" poster="{{ '/assets/img/robots/tecobot/hero.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>TeCoBot.</strong> One soft robot that inches, crawls, rolls, turns, and climbs inside a pipe.</div>
  </div>
</div>

## Related robots

- [Tensegrity-Wheeled Jumping Robot]({{ '/robots/tensegrity-wheels/' | relative_url }}): rolls, changes shape, and jumps over obstacles.
- [TeCoBot]({{ '/robots/tecobot/' | relative_url }}): soft tensegrity robots with six ways to move on their own and more as a team.

## Publications

<div class="publications">
{% bibliography --group_by none --query @*[area~=multimodal] %}
</div>
