---
layout: page
title: Origami-Inspired Reconfigurable Robot
description: A four-legged robot built from origami-inspired modules whose joints switch between soft and rigid, so the same legs can walk, crawl, inch, or grasp.
img: assets/img/robots/origami-modules/card.jpg
card_video: assets/video/robots/origami-modules/card.mp4
year: 2022
venue: IEEE/ASME Transactions on Mechatronics
order: 5
related_publications: true
---

<img class="img-fluid rounded z-depth-1 mb-3 d-block mx-auto" style="max-width: 80%;" src="{{ '/assets/img/robots/origami-modules/robot.jpg' | relative_url }}" alt="The four-legged reconfigurable robot built from origami-inspired modules">

A frog walks, jumps, swims, and climbs with the same body and legs, just held in different configurations. Most robots, in contrast, need a separate mechanism for each way of moving. This robot takes the frog's approach: its legs are stacks of small **origami-inspired modules** whose joints can each be made **soft or rigid**. Pulling the same tendon then produces a different motion depending on which joints are soft, so the same four legs can **walk, crawl, inch, or act as arms to grasp**.

<p class="robot-links">
  <a class="btn btn-sm z-depth-0" role="button" href="https://doi.org/10.1109/TMECH.2022.3175145">Paper</a>
  <a class="btn btn-sm z-depth-0" role="button" href="https://doi.org/10.1109/TMECH.2026.3700119">Follow-up (2026)</a>
</p>

## At a glance

| Feature | Detail |
| --- | --- |
| Module | Two triangular plates (45 mm sides) joined by three vertical links and three diagonal links, driven by a tendon |
| Joint | Shape-morphing variable-stiffness joint: a PLA rod in an elastic tube, softened by a heating wire |
| Module motions | Collapse, bend, or slant under the same tendon pull, depending on which joints are soft |
| Model | Kinematic model predicts the module's motion with a mean error of 2.4 mm |
| Robot | Four legs, each made of four modules in series |
| Locomotion | Walking (28 mm/s), crawling (21 mm/s), crawling while grasping with two legs (21 mm/s), and inching |

## The module and its joints

<div class="row">
  <div class="col-sm-6 mt-3">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/robots/origami-modules/module.jpg' | relative_url }}" alt="A single origami-inspired module" loading="lazy">
  </div>
  <div class="col-sm-6 mt-3 d-flex align-items-center">
    <img class="img-fluid d-block mx-auto" style="max-height: 300px;" src="{{ '/assets/img/robots/origami-modules/svj-diagram.jpg' | relative_url }}" alt="How a shape-morphing variable-stiffness joint is bent into a new shape and frozen there" loading="lazy">
  </div>
</div>

Each module is a pair of triangular plates connected by three vertical links and three diagonal links. Each diagonal link has a **shape-morphing variable-stiffness joint**: a thermoplastic (PLA) rod inside an elastic tube, wrapped with a heating wire. Three volts heat the rod soft in about 20 seconds so the joint can bend; when it cools, the joint becomes rigid again, either straight or frozen in its new bent shape (right).

A single tendon pulls the top plate down. Which joints are soft decides what happens:

<div class="row">
  <div class="col-sm-4 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/module-collapse.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/module-collapse.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">All three joints soft: the module collapses flat.</div>
  </div>
  <div class="col-sm-4 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/module-bend.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/module-bend.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">Two joints soft: the module bends.</div>
  </div>
  <div class="col-sm-4 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/module-slant.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/module-slant.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">One joint soft: the module slants.</div>
  </div>
</div>

Stacking modules multiplies the options. Two modules in series can collapse or bend either module, or both, giving a much larger set of shapes and motions from one tendon.

<video class="lab-media rounded z-depth-1 mt-3" src="{{ '/assets/video/robots/origami-modules/two-modules.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/two-modules.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">Motions of two modules connected in series.</div>

## A robot that walks, crawls, inches, and grasps

The robot has a three-part body and four legs, each made of four modules in series and driven by a tendon. By choosing which joints are rigid in each leg, the same robot moves in different ways:

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/walking.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/walking.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Walking</strong> with upright legs, at 28 mm/s.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/crawling.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/crawling.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Crawling</strong> with the body low to the ground, at 21 mm/s.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/crawl-grasp.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/crawl-grasp.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Crawling while grasping:</strong> the front legs hold an object while the rear legs crawl.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/origami-modules/inching.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/inching.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption"><strong>Inching</strong> between two walls, about 60 mm per cycle.</div>
  </div>
</div>

<div class="row mt-3">
  <div class="col-sm-6 d-flex align-items-center">
    <p>For these robot demonstrations, the heated joints were replaced by small clips that make a joint soft or hold it rigid, straight or bent, and the legs were reconfigured by hand between modes. Using the heated joints throughout would let the robot reconfigure itself without manual help.</p>
  </div>
  <div class="col-sm-6">
    <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/robots/origami-modules/clip-replacement.jpg' | relative_url }}" alt="A heated joint replaced by a soft clip or a rigid clip" loading="lazy">
  </div>
</div>

## Follow-up: learning the best stiffness for a task (2026)

In the original robot, we picked which joints to make soft by trial and error. In a follow-up study with collaborators at UMass Amherst, we let a computer decide. Using a two-module, tendon-driven manipulator, a **reinforcement learning** framework in the MuJoCo physics simulator learns the **joint stiffnesses and the tendon control policy together** for a reaching task. The learned stiffnesses are built into a physical prototype with fixed-stiffness joints, and the learned controller transfers directly: the real manipulator reaches its targets repeatably, with a final position error below 2 mm.

<img class="img-fluid rounded z-depth-1 mt-3" src="{{ '/assets/img/robots/origami-modules/coopt-framework.jpg' | relative_url }}" alt="Co-optimizing stiffness and control in simulation, then transferring to the prototype" loading="lazy">

<div class="row">
  <div class="col-6 mt-3">
    <video class="img-fluid rounded z-depth-1 d-block mx-auto" style="max-height: 400px;" src="{{ '/assets/video/robots/origami-modules/coopt-sim.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/coopt-sim.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption text-center">Reaching in simulation.</div>
  </div>
  <div class="col-6 mt-3">
    <video class="img-fluid rounded z-depth-1 d-block mx-auto" style="max-height: 400px;" src="{{ '/assets/video/robots/origami-modules/coopt-real.mp4' | relative_url }}" poster="{{ '/assets/video/robots/origami-modules/coopt-real.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption text-center">The same reach on the prototype (2× speed).</div>
  </div>
</div>

## Team

[Zhe Chen]({{ '/people/' | relative_url }}), [Brandon Tighe]({{ '/people/' | relative_url }}), and [Jianguo Zhao]({{ '/people/' | relative_url }}) {% cite chen2022origami %}. The follow-up was done with Li Chen and Hao Zhang at the University of Massachusetts Amherst {% cite chen2026cooptimizing %}. This work was part of Zhe Chen's Ph.D. dissertation.
