---
layout: page
title: Shape-Morphing Robots
description: Robots that change their own shape and then lock it in place, with the actuation, sensing, and locking all built into the body. Grippers, a quadruped, and an amphibious robot share one method.
img: assets/img/robots/shape-morphing/card.jpg
card_video: assets/video/robots/shape-morphing/card.mp4
year: 2023
venue: Nature Communications
order: 3
related_publications: true
---

<video class="lab-media rounded z-depth-1 mb-3" src="{{ '/assets/video/robots/shape-morphing/smart-river.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/smart-river.jpg' | relative_url }}" autoplay loop muted playsinline></video>

Animals such as frogs change their body shape as they grow, from swimming tadpoles to walking adults. Robots that can change shape the same way could adapt to new tasks and environments, but most shape-morphing robots need bulky pumps, magnets, or external sensors to do it. We developed a way to put everything **inside the robot's body**: a muscle-like actuator that bends the body and senses how far it has bent, and a spine that turns soft to let the shape change and then hardens to **lock the new shape in place without using any more power**.

Using the same building block, we made several robots: grippers that reshape their palm to fit the object, a lightweight quadruped that reshapes its body to crawl, walk, or climb along a beam, and **SMART**, an untethered amphibious robot that turns its flippers into legs to walk out of a river.

<p class="robot-links">
  <a class="btn btn-sm z-depth-0" role="button" href="https://doi.org/10.1038/s41467-023-41708-6">Paper (open access)</a>
</p>

## At a glance

| Feature | Detail |
| --- | --- |
| Building block | 115 mm bending module: a shape-memory-polymer spine with a heating wire, plus a sheathed twisted-and-coiled actuator (TCA) |
| Locking | The spine is about 67 times softer when heated above 100 °C, and rigid again once it cools |
| Actuation and sensing | The TCA contracts when powered and its electrical resistance reports how far the module has bent |
| Speed | Bends up to 240° in one second when soft; feedback control reaches a target angle more than 10× faster than open-loop |
| Robots | Two morphing grippers, a 28 g quadruped, and SMART, an untethered amphibious robot |
| Module library | Twisting, 3D bending, twisting and bending, discrete surface, and grid surface modules |

## The shape-morphing module

<video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/module.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/module.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">Straight and rigid, then heated soft, bent by the artificial muscle, cooled, and holding its new shape. The inset is a thermal camera view.</div>

Each module has two parts that do different jobs:

- A **spine** cast from a custom shape memory polymer (SMP), wrapped with a heating wire and fitted with a temperature sensor. Cold, it is rigid enough to hold a 15 g weight. Heated, it becomes soft and flexible. Because of its shape memory, reheating it also returns it to its original straight shape.
- A **twisted-and-coiled actuator** (TCA), an artificial muscle made from sewing thread that contracts when a few volts are applied, sealed in a soft silicone tube and attached to small posts along the spine. Its electrical resistance changes as it contracts, so the muscle doubles as a bend sensor, with no extra sensors needed.

To change shape, the spine is heated soft, the muscle bends the module to the target angle using its own resistance as feedback, and the spine cools to lock the shape. After that, the module holds its shape with no power at all.

<img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/research/embedded-morphing-fig1.jpg' | relative_url }}" alt="One morphing module with embedded actuation, sensing, and locking can form a morphing body, limb, or base" loading="lazy">

## Morphing grippers

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/gripper-pinch.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/gripper-pinch.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">The palm bends so the fingers can reach and pinch a sponge.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/gripper-cage.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/gripper-cage.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">A cross-shaped palm locks around an egg and holds it with no power.</div>
  </div>
</div>

In the first gripper, a module serves as the palm between two soft fingers. A rigid palm only lets the fingers grasp objects between 111 and 126 mm wide; by bending the palm first, the morphing gripper handles objects from 20 to 126 mm, from a ping pong ball to a sponge.

The second gripper uses two modules in a cross to cage objects such as a spool of thread, a computer mouse, or an egg. Once the modules have locked, the gripper holds the object without using any energy, so for any grasp longer than about two minutes it uses less energy than a soft gripper that has to stay powered.

## A quadruped that reshapes its body

<video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/quadruped.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/quadruped.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">Crawling under a glass plate, standing up to walk, then narrowing its body to climb along a beam (2× the speed of the original movie).</div>

Three modules form the body of a quadruped that weighs only 28 g without its control board, with four soft continuum legs. Changing the body shape changes how it moves:

- **Flat (250 mm wide, 28 mm tall):** it crawls under low obstacles.
- **Standing (150 mm wide, 120 mm tall):** it walks more than six times faster.
- **Narrow (80 mm wide):** its feet clamp both sides of a 6.5 mm beam, so it can climb along a narrow bridge.

<img class="img-fluid rounded z-depth-1 d-block mx-auto" style="max-width: 75%;" src="{{ '/assets/img/robots/shape-morphing/fig5-quadruped.jpg' | relative_url }}" alt="Design of the quadruped and its three body shapes for crawling, walking, and climbing" loading="lazy">

## SMART: an amphibious robot that turns flippers into legs

<video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/smart-tank.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/smart-tank.jpg' | relative_url }}" autoplay loop muted playsinline></video>
<div class="caption">SMART swims with straight flippers, lifts them out of the water to curve them, dips them to cool, and walks up onto the shore.</div>

The Shape-Morphing Amphibious RoboT (SMART) carries its battery, electronics, and motors inside a sealed 145 × 120 × 58 mm body, so it needs no tether. Each of its four legs is a morphing module turned by a motor. Straight legs work as flippers for swimming; curved legs work as limbs for walking. Dipping the hot legs in water cools and locks them in about a second.

Outdoors, at about 3 °C, SMART walked across a rock, straightened its legs at the river's edge, pushed off, and swam away (see the video at the top of this page).

<img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/robots/shape-morphing/fig6-smart.jpg' | relative_url }}" alt="SMART design, leg drive train, electronics, and indoor and outdoor demonstrations" loading="lazy">

## A library of morphing modules

The same recipe of SMP spine plus TCA works for other shapes too. Arranging the muscles differently gives modules that twist, bend in any 3D direction, or curl into a helix. Using an SMP surface instead of a spine gives sheets and grids that fold into several different shapes.

<div class="row">
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/module-3d-bending.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/module-3d-bending.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">A 3D bending module with three muscles bends in any direction.</div>
  </div>
  <div class="col-sm-6 mt-3">
    <video class="lab-media rounded z-depth-1" src="{{ '/assets/video/robots/shape-morphing/module-grid.mp4' | relative_url }}" poster="{{ '/assets/video/robots/shape-morphing/module-grid.jpg' | relative_url }}" autoplay loop muted playsinline></video>
    <div class="caption">A grid surface takes different shapes depending on which edges are pulled.</div>
  </div>
</div>

<div class="caption">Videos and figures are from Sun et al., <em>Nature Communications</em> (2023), published open access under CC BY 4.0. Most videos are sped up in the original movies.</div>

## Team

[Jiefeng Sun]({{ '/people/' | relative_url }}), [Elisha Lerner]({{ '/people/' | relative_url }}), [Brandon Tighe]({{ '/people/' | relative_url }}), [Clint Middlemist]({{ '/people/' | relative_url }}), and [Jianguo Zhao]({{ '/people/' | relative_url }}) {% cite sun2023embedded %}.
