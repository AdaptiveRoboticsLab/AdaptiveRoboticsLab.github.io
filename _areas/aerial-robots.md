---
layout: page
title: Aerial Robots
description: Small flying robots that perch on branches, walls, and ceilings to save energy, and grasp objects in flight.
img: assets/video/research/tunable-perching.jpg
card_video: assets/video/research/tunable-perching.mp4
order: 3
area_key: aerial
---

<video class="lab-media rounded z-depth-1 mb-3" src="{{ '/assets/video/research/hybrid-perching.mp4' | relative_url }}" poster="{{ '/assets/video/research/hybrid-perching.jpg' | relative_url }}" autoplay loop muted playsinline></video>

Small drones can only stay in the air for a few minutes because hovering uses a lot of energy. Birds and insects solve this by **perching**. If a drone can perch on a branch, a wall, or a ceiling, it can save or even harvest energy while it watches, measures, or inspects. We study how small aerial robots can perch reliably and how they can pick up and carry objects.

## Questions we work on

- **Mechanical intelligence.** Can a gripper close by itself the moment it touches a target, with no sensing or power? We use bistable mechanisms that snap shut on impact and hold with no energy.
- **Perching on any surface.** How can one mechanism perch on both branches and flat surfaces, even when the drone arrives fast or at a large tilt?
- **Seeing and landing.** How do flies land upside down on a ceiling, and how can a robot use vision, such as time-to-contact, to time its landing?
- **Aerial grasping.** How can a drone grasp and carry objects with a compliant gripper and an adaptive controller?

## Key results

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/bistable-perching.mp4' | relative_url }}" poster="{{ '/assets/video/research/bistable-perching.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Compliant bistable grippers.</strong> A micro aerial vehicle perches passively on a pipe.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="img-fluid d-block mx-auto rounded z-depth-1" style="max-height: 300px;" src="{{ '/assets/video/research/mip-gripper.mp4' | relative_url }}" poster="{{ '/assets/video/research/mip-gripper.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption text-center"><strong>A mechanically intelligent gripper</strong> closes on the bar as the drone flies into it.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/tunable-perching.mp4' | relative_url }}" poster="{{ '/assets/video/research/tunable-perching.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Tunable perching.</strong> Tuning the mechanism lets a drone perch on a surface tilted 25° and hit at speed (slow motion).</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/spring-steel-gripper.mp4' | relative_url }}" poster="{{ '/assets/video/research/spring-steel-gripper.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Bistable spring-steel grippers</strong> snap closed on contact and hold with no power.</div>
  </div>
</div>

The video at the top shows our hybrid perching mechanism landing on both a tree branch and flat surfaces.

## Publications

<div class="publications">
{% bibliography --group_by none --query @*[area~=aerial] %}
</div>
