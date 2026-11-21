---
layout: page
title: Stiffness-Programmable Origami Robot
description: A 3D-printed, three-fingered origami robot that grasps and walks in different ways under the same motor commands, just by changing how stiff its creases are.
img: assets/img/robots/origami/card.jpg
card_video: assets/video/robots/origami/card.mp4
year: 2026
venue: Advanced Robotics Research
order: 2
related_publications: true
---

<img class="img-fluid rounded z-depth-1 mb-3" src="{{ '/assets/img/robots/origami/fig1-overview.jpg' | relative_url }}" alt="Overview: origami base unit with stiffness inserts, the origami finger, the three-fingered robot, and its grasping and locomotion">
<div class="caption">From one printed base unit to a three-fingered robot that grasps objects and changes its gait to pass under a gap.</div>

Origami robots fold flat sheets into moving structures, but making one structure do many different things usually means adding more motors. This robot takes a different route: every finger is pulled by a **single tendon**, and what the finger does depends on **how stiff each crease is**. Swap a few small inserts, or heat one of them, and the same motor command makes the finger curl, hook, twist, or stay flat. With three such fingers, the robot can grasp objects from strawberries to a 480-gram cucumber, and it can walk with two different gaits.

<p class="robot-links">
  <a class="btn btn-sm z-depth-0" role="button" href="https://doi.org/10.1002/adrr.70158">Paper (open access)</a>
  <a class="btn btn-sm z-depth-0" role="button" href="https://doi.org/10.1098/rsta.2024.0017">Earlier paper (2024)</a>
</p>

## At a glance

| Feature | Detail |
| --- | --- |
| Structure | Modified Yoshimura origami, printed in one piece: rigid PETG panels joined by soft TPU creases |
| Stiffness control | Swappable inserts on each crease: locking, fixed-stiffness, or heated variable-stiffness |
| Actuation | One tendon per finger, driven by a geared DC motor with an encoder |
| Robot size | 330 mm across and 50 mm tall when relaxed; three fingers on a soft TPU palm |
| Grasping | Paper roll, 454 g wire spool, foam globe, strawberry, spray bottle, cucumber, box, pear |
| Locomotion | Crawling (24 mm per cycle, 80 mm tall) and crutching (69 mm per cycle, 120 mm tall) |

## How it is built

Each building block is a pair of rigid triangular panels joined by a soft crease, made in a single print on a regular multimaterial FDM 3D printer, with no assembly of the hinge. Each crease has a slot for a small **stiffness insert**:

- a **locking insert** (PLA) that stops the crease from bending;
- a **fixed-stiffness insert**, a TPU strip between two PLA plates, whose thickness sets how stiff the crease is;
- a **variable-stiffness insert**, a layered shape-memory-polymer and PVC strip with a heating wire and temperature sensor. Heating it softens it to roughly a quarter of its room-temperature stiffness, so a crease can switch between stiff and soft while the robot runs.

<img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/robots/origami/fig2-inserts.jpg' | relative_url }}" alt="Stiffness insert designs and measured bending stiffness" loading="lazy">
<div class="caption">The three insert types and their measured stiffness: thicker fixed inserts are stiffer (E), and the variable insert softens as it heats (F).</div>

The finger is a flattened section of a Yoshimura origami pattern with three bending creases, two diagonal creases for twisting, and two clamping creases at the tip. A thin metal tendon runs through small guides on the panels, so one motor pulls on all the creases at once. The stiffness pattern decides which creases give way first.

<img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/robots/origami/fig3-finger.jpg' | relative_url }}" alt="Finger origami pattern and tendon routing" loading="lazy">
<div class="caption">The finger's crease layout (A) and tendon routing (B). Each finger is 128 mm by 123 mm.</div>

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="img-fluid d-block mx-auto rounded" style="max-height: 420px;" src="{{ '/assets/video/robots/origami/bending.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/bending.jpg' | relative_url }}" autoplay loop muted playsinline></video>
  </div>
  <div class="col-sm-6 mt-3 d-flex align-items-center">
    <p>Same finger, same tendon pull, different inserts: as the inserts on the bending creases change (labels at top, insert thickness in mm), the finger bends at a different crease and ends in a different shape.</p>
  </div>
</div>

A simple model, based on the finger's geometry and the tendon tension, predicts how much each crease bends for a given tendon pull, and experiments match it across the stiffness patterns we tested.

## Grasping

With the same stiffness pattern on all three fingers, the robot can be set up for a specific object: a short pattern for a paper roll, a hooked pattern to lift a 454 g wire spool by its rim, and a curved pattern to wrap around a foam globe. Softer patterns let the fingers simply conform, which is enough to cradle a strawberry or hold a spray bottle.

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/grasp-sym.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/grasp-sym.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Same pattern on every finger: a wire spool and a foam globe (3× speed).</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/grasp-cucumber.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/grasp-cucumber.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Different pattern on each finger: a pincer grip on a 480 g cucumber (5× speed).</div>
  </div>
</div>

<img class="img-fluid rounded z-depth-1 mt-3" src="{{ '/assets/img/robots/origami/fig6-grasping.jpg' | relative_url }}" alt="Grasping a paper roll, wire spool, foam globe, strawberry, and spray bottle" loading="lazy">

Giving each finger a different pattern unlocks more specialized grips: a pincer grip on a heavy cucumber, a parallel grip on a cracker box with two twisting fingers, and a gentle cradle for a pear.

<img class="img-fluid rounded z-depth-1 d-block mx-auto" style="max-width: 60%;" src="{{ '/assets/img/robots/origami/fig7-asymmetric.jpg' | relative_url }}" alt="Grasping a cucumber, a box, and a pear with different patterns on each finger" loading="lazy">

With variable-stiffness inserts, the robot changes its grip without anyone touching it. Cold, the inserts keep the fingers flat for clamping a box or a ball; heated, the fingers curl around a cylindrical tea canister that the flat grip cannot hold.

<video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/grasp-vsi.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/grasp-vsi.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">Top: inserts cold, fingers stay flat. Bottom: inserts heated (see the thermal image), fingers curl (2× speed).</div>

<img class="img-fluid rounded z-depth-1 mt-3" src="{{ '/assets/img/robots/origami/fig8-vsi-grasping.jpg' | relative_url }}" alt="Grasping with variable-stiffness inserts unheated and heated, with thermal images" loading="lazy">

## Walking

The same three fingers can also walk. One finger pushes while the other two support the body. Where the stiffness pattern stores elastic energy decides the gait: bending the tip creases gives a low, steady **crawl** (about 24 mm per cycle, 80 mm tall), while bending the base creases gives a taller, longer-striding **crutching** gait (about 69 mm per cycle, 120 mm tall).

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/crawl.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/crawl.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Crawling.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/crutch.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/crutch.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Crutching.</div>
  </div>
</div>

<img class="img-fluid rounded z-depth-1 mt-3" src="{{ '/assets/img/robots/origami/fig9-gaits.jpg' | relative_url }}" alt="Crawling and crutching gaits with stride and height comparison" loading="lazy">

Heating a single variable-stiffness insert switches the gait on the spot. Crutching is too tall to fit under a 90 mm gap; after the insert is heated, the robot drops to a crawl and passes underneath, with the same motor commands throughout.

<video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/gait-switch.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/gait-switch.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">Crutching, heating one insert, then crawling under the gap (2× and 5× speed, as labeled).</div>

<img class="img-fluid rounded z-depth-1 mt-3" src="{{ '/assets/img/robots/origami/fig10-gait-switch.jpg' | relative_url }}" alt="Heating one insert switches from crutching to crawling to pass under a 90 mm gap" loading="lazy">

<div class="caption">All figures and videos above are from Lerner and Zhao, <em>Advanced Robotics Research</em> (2026), published open access under CC BY 4.0. Videos are sped up as labeled.</div>

## Earlier version: variable-stiffness joints (2024)

This robot builds on our earlier origami module with four variable-stiffness joints, each a thermoplastic layer sandwiched between shape-memory-polymer layers and softened by Joule heating. Two of those modules formed a small robot that could inch, undulate, and crawl like a turtle, and the same pair worked as an adaptive gripper.

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/early-gripper.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/early-gripper.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">The 2024 modules used as a gripper on a jar (3× speed).</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami/early-inchworm.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami/early-inchworm.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">The 2024 two-module robot inching forward.</div>
  </div>
</div>

## Team

[Elisha Lerner]({{ '/people/' | relative_url }}) and [Jianguo Zhao]({{ '/people/' | relative_url }}) {% cite lerner2026stiffness %}. The earlier version was developed with [Zhe Chen]({{ '/people/' | relative_url }}) {% cite lerner2024origami %}.
