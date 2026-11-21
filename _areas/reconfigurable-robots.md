---
layout: page
title: Reconfigurable Robots
description: One body, many functions. Variable-stiffness joints, origami and tensegrity modules, and robots that link up into new shapes.
img: assets/img/robots/tecobot/card.jpg
card_video: assets/video/robots/tecobot/card.mp4
order: 2
area_key: reconfigurable
---

<video class="lab-media rounded z-depth-1 mb-3" src="{{ '/assets/video/robots/tecobot/moving.mp4' | relative_url }}" poster="{{ '/assets/img/robots/tecobot/card.jpg' | relative_url }}" autoplay loop muted playsinline></video>

Most robots use each body part for one job, fixed by their mechanical design. Our reconfigurable robots can change how their parts are arranged or how stiff their joints are, so the **same hardware** can walk, crawl, grasp, or roll, and several robots can join into a larger one.

## Questions we work on

- **Programming motion with stiffness.** If some joints are soft and others rigid, the same actuator produces different motions. How do we design joints whose stiffness can be set, and even changed while the robot runs?
- **Modular structures.** How can origami-inspired and tensegrity modules be stacked and combined into legs, fingers, and bodies with many possible shapes?
- **Choosing the best configuration.** Given a task, which stiffness or shape should the robot take? We use models and learning to choose the configuration and the controller together.
- **Robots that join together.** How can individual robots dock with one another to form chains, loops, and branches that do what one robot cannot?

## Key results

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/adaptive-walking.mp4' | relative_url }}" poster="{{ '/assets/video/research/adaptive-walking.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Shape-morphing joints.</strong> A walking robot reconfigures its legs to step over an obstacle.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/walking.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/walking.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Origami-inspired modules.</strong> The same four legs can walk, crawl, inch, or grasp.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/gait-switch.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/gait-switch.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Stiffness-programmable origami.</strong> Heating one insert switches the robot's gait so it fits under a gap.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/manipulate.mp4' | relative_url }}" poster="{{ '/assets/img/robots/tecobot/lift-ball.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Modular tensegrity robots.</strong> TeCoBots link up to manipulate objects together.</div>
  </div>
</div>

## Related robots

- [TeCoBot]({{ '/robots/tecobot/' | relative_url }}): soft tensegrity robots that link into new shapes.
- [Stiffness-Programmable Origami Robot]({{ '/robots/origami-robot/' | relative_url }}): a three-fingered origami robot that grasps and walks.
- [Origami-Inspired Reconfigurable Robot]({{ '/robots/origami-modules/' | relative_url }}): a four-legged robot built from origami modules.

## Publications

<div class="publications">
{% bibliography --group_by none --query @*[area~=reconfigurable] %}
</div>
