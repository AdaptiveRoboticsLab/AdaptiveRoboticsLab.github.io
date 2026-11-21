---
layout: page
title: Tensegrity-Wheeled Jumping Robot
description: A lightweight robot that rolls on tensegrity wheels, squeezes them flat to change its shape, and jumps over obstacles with a snap-through spring.
img: assets/img/robots/tensegrity-wheels/card.jpg
card_video: assets/video/robots/tensegrity-wheels/card.mp4
year: 2023
venue: IEEE/ASME Transactions on Mechatronics
order: 4
related_publications: true
---

<video class="lab-media rounded z-depth-1 mb-3" src="{{ '/assets/video/robots/tensegrity-wheels/overview.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/overview.jpg' | relative_url }}" autoplay loop muted playsinline></video>

Small robots for search and rescue or exploration need to cross rocks, steps, gaps, and soft ground, and survive falls. This robot rolls on two **tensegrity wheels**, open frames of carbon-fiber rods held together by elastic cables. The wheels are light, springy, and shock-absorbing, and they can be **squeezed into flat disks** to make the robot narrower and taller. A **bistable spring** under the body stores energy slowly and releases it in a snap, letting the robot **jump onto obstacles up to 300 mm high**.

<p class="robot-links">
  <a class="btn btn-sm z-depth-0" role="button" href="https://doi.org/10.1109/TMECH.2023.3276933">Paper</a>
</p>

## At a glance

| Feature | Detail |
| --- | --- |
| Size | About 500 mm long, 400 mm wide, and 100 mm tall |
| Wheels | Two icosahedron tensegrity wheels: six 2 mm carbon-fiber rods and 3D-printed TPU elastic cables each |
| Shape change | Collapsing the wheels shrinks the width from 400 to 180 mm and raises the body from 75 to 95 mm |
| Climbing | Steps up to 110 mm with expanded wheels and 150 mm with collapsed wheels; slopes up to 45° |
| Jumping | Bistable mechanism jumps onto obstacles up to 300 mm high |
| Speed and payload | Up to 0.36 m/s; carries about six times its own weight |

## Tensegrity wheels that change shape

<img class="img-fluid rounded z-depth-1 d-block mx-auto" style="max-width: 75%;" src="{{ '/assets/img/robots/tensegrity-wheels/robot-labeled.jpg' | relative_url }}" alt="The robot with its tensegrity wheels, jumping mechanism, and tail labeled" loading="lazy">

Each wheel is an icosahedron tensegrity: six stiff rods that never touch each other, held in shape by a network of stretchy cables. The cable network is 3D printed flat in soft TPU and then fitted onto the rods, so a wheel is cheap and quick to make. Because the whole wheel can flex, it absorbs impacts and conforms to rough ground without adding weight.

<img class="img-fluid rounded z-depth-1 mt-3" src="{{ '/assets/img/robots/tensegrity-wheels/wheel-fabrication.jpg' | relative_url }}" alt="The flat 3D-printed cable network, assembling it onto the rods, and the finished wheel" loading="lazy">
<div class="caption">The cable network is printed flat (left), then fitted onto the rods to form the wheel (right).</div>

A small motor and pulley inside each hub pull the wheel's two sides together, collapsing it into a disk. That makes the robot 55% narrower, so it can squeeze through tight gaps, and lifts its body higher off the ground.

<div class="row">
  <div class="col-sm-6 mt-3">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/robots/tensegrity-wheels/shape-change.jpg' | relative_url }}" alt="Front view comparing expanded and collapsed wheels" loading="lazy">
    <div class="caption">Expanded wheels (outer outline) and collapsed wheels: narrower and taller.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/collapse-fea.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/collapse-fea.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Measuring the force to collapse a wheel, next to a simulation of the same test.</div>
  </div>
</div>

The wheels' rods also act like the spokes of a wheel-leg, catching the edge of a step. We built models that predict the tallest step a tensegrity wheel can climb, giving other designers a guide for sizing their own wheels. In tests the robot climbed steps up to 110 mm with expanded wheels and 150 mm with collapsed wheels.

<video class="lab-media rounded z-depth-1 mt-3" src="{{ '/assets/video/robots/tensegrity-wheels/step-climb.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/step-climb.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">Climbing steps of different heights with expanded and collapsed wheels.</div>

## Jumping with a bistable spring

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="img-fluid d-block mx-auto rounded z-depth-1" style="max-height: 380px;" src="{{ '/assets/video/robots/tensegrity-wheels/jump-mechanism.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/jump-mechanism.jpg' | relative_url }}" autoplay loop muted playsinline></video>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/jump.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/jump.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <p class="mt-3">A motor slowly loads a bistable mechanism until it snaps through to its other stable state, driving a foot hard against the ground. Storing energy slowly and releasing it all at once lets a small motor launch the whole robot onto a ledge, as high as 380 mm in this test.</p>
  </div>
</div>

## Testing on slopes, obstacles, and natural terrain

<div class="row">
  <div class="col-6 mt-3">
    <video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/slope-45.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/slope-45.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">A 45° slope on a high-friction mat.</div>
  </div>
  <div class="col-6 mt-3">
    <video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/slope-40.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/slope-40.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">A 40° slope on smoother foam.</div>
  </div>
</div>

In an obstacle course, the robot drove over a rock pile, jumped a 250 mm wall, crossed a rolling pipe and a 200 mm gap, climbed a 100 mm step, and went up a slope.

<video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/obstacle-course.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/obstacle-course.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">The obstacle course (2× speed).</div>

Outdoors, the robot rolled across snow, ice, grass, gravel, mulch, and sand, and changed its shape in tall grass.

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/terrains.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/terrains.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Snow, ice, grass, gravel, mulch, and sand.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/tensegrity-wheels/field-shape-change.mp4' | relative_url }}" poster="{{ '/assets/video/robots/tensegrity-wheels/field-shape-change.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Driving and changing shape outdoors.</div>
  </div>
</div>

## Team

[Sydney Spiegel]({{ '/people/' | relative_url }}), [Jiefeng Sun]({{ '/people/' | relative_url }}), and [Jianguo Zhao]({{ '/people/' | relative_url }}) {% cite spiegel2023tensegrity %}. Sydney led this work as an undergraduate researcher in the lab and won the top prize at CSU Demo Day with the robot.
