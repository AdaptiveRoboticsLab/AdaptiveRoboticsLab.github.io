---
layout: page
title: Soft Robots
description: Artificial muscles, soft bodies that switch between soft and rigid, and robots that change their shape and lock it in place.
img: assets/video/research/tca-soft-arm.jpg
card_video: assets/video/research/tca-soft-arm.mp4
order: 1
area_key: soft
---

<video class="lab-media rounded z-depth-1 mb-3" src="{{ '/assets/video/robots/shape-morphing/module.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/module.jpg' | relative_url }}" autoplay loop muted playsinline></video>

Soft robots have deformable bodies and muscle-like actuators, so they can bend, squeeze, and conform to their surroundings in ways rigid robots cannot. We include **shape morphing** here: to change shape, a robot's body first has to become soft, and then it needs a way to hold its new shape.

## Questions we work on

- **Artificial muscles.** How can cheap, lightweight actuators made from sewing thread, called twisted-and-coiled actuators (TCAs), drive soft robots? How do we model them from physics and control them, including using the muscle itself as a sensor?
- **Fast and strong soft motion.** Soft robots tend to be slow and weak. Can elastic instabilities and bistable structures, which store energy and release it in a snap, make them both fast and strong?
- **Shape morphing.** How can a robot soften its body, move into a new shape, and then lock that shape in place without external pumps or magnets, and without using power to hold it?

## Key results

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/tca-soft-arm.mp4' | relative_url }}" poster="{{ '/assets/video/research/tca-soft-arm.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Soft robots driven by TCAs.</strong> A soft arm driven by twisted-and-coiled actuators with free strokes grips and moves a part.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/research/embedded-shape-morphing.mp4' | relative_url }}" poster="{{ '/assets/video/research/embedded-shape-morphing.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Controllable shape morphing.</strong> A link that softens, bends with a TCA, and locks changes the path of a mechanism.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/smart-tank.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/smart-tank.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Embedded shape morphing.</strong> An amphibious robot turns its straight flippers into curved legs to walk out of the water.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/gripper-pinch.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/gripper-pinch.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Morphing grippers.</strong> A gripper reshapes its palm to fit objects from 20 to 126 mm wide.</div>
  </div>
</div>

We have also built physics-based models of TCAs using Cosserat rod theory, controlled soft robot shapes with the Koopman operator, used elastic instabilities for fast and strong soft robots, and manipulated liquid droplets with a soft gripper.

## Related robots

- [Shape-Morphing Robots]({{ '/robots/shape-morphing/' | relative_url }}): grippers, a quadruped, and an amphibious robot that morph and lock their shape.

## Publications

<div class="publications">
{% bibliography --group_by none --query @*[area~=soft] %}
</div>
