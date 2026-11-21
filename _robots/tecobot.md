---
layout: page
title: TeCoBot
description: Soft, snake-like robots built from tensegrity modules that link up into chains, loops, and branches to do what one robot can't.
img: assets/img/robots/tecobot/card.jpg
card_video: assets/video/robots/tecobot/card.mp4
year: 2026
venue: Nature Machine Intelligence
order: 1
related_publications: true
---

<img class="img-fluid rounded z-depth-1 mb-3" src="{{ '/assets/img/robots/tecobot/hero.jpg' | relative_url }}" alt="Three TeCoBots standing, one of them bending to the side">

**TeCoBot** (**Te**nsegrity-based **Co**ntinuum ro**Bot**) is a soft, modular robot with a claw at each end. One TeCoBot can grab objects, inch like a worm, roll over rocks, and climb inside a pipe. The claw that grabs objects can also grab another TeCoBot, so a team of robots can link into chains, loops, an H shape, or a four-robot "lizard" and take on tasks that no single robot can do alone.

<p class="robot-links">
  <a class="btn btn-sm z-depth-0" role="button" href="https://doi.org/10.1038/s42256-026-01335-4">Paper</a>
  <a class="btn btn-sm z-depth-0" role="button" href="https://arxiv.org/abs/2608.27221">arXiv</a>
  <a class="btn btn-sm z-depth-0" role="button" href="https://tecobot.github.io">Project site</a>
  <a class="btn btn-sm z-depth-0" role="button" href="https://github.com/mahmud-hasans/TeCoBot">Code</a>
  <a class="btn btn-sm z-depth-0" role="button" href="https://youtu.be/AmEtvBz54M4">Video</a>
</p>

<div class="video-embed rounded z-depth-1 mb-3">
  <iframe
    src="https://www.youtube-nocookie.com/embed/AmEtvBz54M4"
    title="TeCoBot: Soft Robots That Link Up Into New Shapes"
    allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
    referrerpolicy="strict-origin-when-cross-origin"
    allowfullscreen
    loading="lazy"
  ></iframe>
</div>

## At a glance

| Feature | Detail |
| --- | --- |
| Body | 4 stacked icosahedral tensegrity modules (carbon-fiber rods + 3D-printed TPU tendons) |
| Size and weight | 587 mm long, 110 mm diameter, about 600 g without batteries |
| Actuation | 3 cables, 120° apart, driven by encoded DC motors in the base |
| Motions | Axial collapse/extension and bending in any direction |
| End effectors | Swappable claws at both ends, driven through a self-locking worm gear |
| Control | Wireless (Wi-Fi) through ESP32-S3 boards; robots can be driven alone or in sync |
| Top speed | 30 mm/s rolling on smooth wood |

## How it is built

<video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/design.mp4' | relative_url }}" poster="{{ '/assets/img/robots/tecobot/design-poster.jpg' | relative_url }}" autoplay loop muted playsinline controls></video>

Each module is an icosahedral tensegrity: six rigid carbon-fiber rods held together by one stretchable tendon network, which is 3D printed flat in TPU and then assembled into 3D. The rods carry compression and the elastic tendon carries tension, so the module is stiff enough to bear loads yet can collapse and bend and then spring back.

Four modules are stacked into a continuum body. Three cables run along the body; pulling them together collapses the robot, and pulling them unequally bends it in any direction. A useful property of stacking is that adding modules increases how far the robot can collapse and bend **without increasing the force** the motors must supply.

A base module holds the motors, encoders, and electronics, and a top module carries the main battery. Each end has a claw. The claws are used both to grasp objects and to dock with other TeCoBots.

<img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/robots/tecobot/fig2-design.jpg' | relative_url }}" alt="Design of TeCoBot: tensegrity modules, base module, claws, and electronics">
<div class="caption">Design of TeCoBot: (a) the full robot, (b) the tensegrity modules, (c) the base module with the cable-driving system, (d) the two claw designs, and (e) wireless control.</div>

## One robot on its own

<video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/single.mp4' | relative_url }}" autoplay loop muted playsinline controls></video>

A single TeCoBot works as a small manipulator: it can pick a grape and drop it into a jar. It can also move in six ways: extending and compressing, inching like a worm, crawling, rolling, turning, and climbing inside a pipe. We tested it on eight outdoor terrains, from grass and gravel to rocks and hay. Rolling worked on almost all of them.

## Linking up and moving together

<video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/moving.mp4' | relative_url }}" autoplay loop muted playsinline controls></video>

TeCoBots dock claw-to-claw or claw-to-body, and they can undock and reconnect in a different shape. Because each robot stays soft after docking, the combined body can still bend and collapse. Different shapes suit different places:

- **Chain**: the middle robot pushes and pulls while the end claws take turns anchoring.
- **Loop**: the robots wrap around a large object, or roll together along a pipe.
- **H shape**: the robots climb through a rectangular duct.
- **Two robots** linked end to end can roll across a gap that one robot cannot cross, and **four robots** can move like a lizard.

<div class="row mt-3">
  <div class="col-sm mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1 robot-photo" src="{{ '/assets/img/robots/tecobot/gap.jpg' | relative_url }}" alt="Two linked TeCoBots rolling across a gap" loading="lazy">
  </div>
  <div class="col-sm mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1 robot-photo" src="{{ '/assets/img/robots/tecobot/logs.jpg' | relative_url }}" alt="Three TeCoBots in a chain crossing a log outdoors" loading="lazy">
  </div>
</div>
<div class="caption">Two linked robots crossing a gap (left), and three robots in a chain crossing a log outdoors (right).</div>

## Working together

<video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/manipulate.mp4' | relative_url }}" autoplay loop muted playsinline controls></video>

When docked to a frame, three TeCoBots can rearrange themselves for different jobs: three hanging robots lift a large ball, two robots pick up a test tube and pour from it, the robots hold a jar while another opens it, and a chain of robots reaches objects too far away for one.

<div class="row mt-3">
  <div class="col-sm mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1 robot-photo" src="{{ '/assets/img/robots/tecobot/lift-ball.jpg' | relative_url }}" alt="Three TeCoBots lifting a red ball together" loading="lazy">
  </div>
  <div class="col-sm mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1 robot-photo" src="{{ '/assets/img/robots/tecobot/open-jar.jpg' | relative_url }}" alt="Two TeCoBots hold a jar while a third opens it" loading="lazy">
  </div>
  <div class="col-sm mt-3 mt-md-0">
    <img class="img-fluid rounded z-depth-1 robot-photo" src="{{ '/assets/img/robots/tecobot/test-tube.jpg' | relative_url }}" alt="TeCoBots picking up a test tube" loading="lazy">
  </div>
</div>
<div class="caption">Lifting a ball, opening a jar, and handling a test tube.</div>

## Real-world tasks

<video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/tasks.mp4' | relative_url }}" autoplay loop muted playsinline controls></video>

Combining these skills, three TeCoBots cleaned up a desk: they lifted one robot onto the table, put a pen back in its holder, handed a piece of scrap paper down the chain, and carried it to the trash bin. In a second task they organized a cabinet, opening a drawer and handing a motor from a supply bin into it.

<video class="img-fluid rounded z-depth-1 mt-3" src="{{ '/assets/video/robots/tecobot/outdoors.mp4' | relative_url }}" autoplay loop muted playsinline controls></video>

Outdoors, linked TeCoBots climbed down to a stream to pick trash out of the water, and rolled a beaker to a bush to collect a plant sample.

## Autonomous docking

<video class="img-fluid rounded z-depth-1" src="{{ '/assets/video/robots/tecobot/docking.mp4' | relative_url }}" autoplay loop muted playsinline controls></video>

In the demonstrations above, a person drives the robots and decides how they reconfigure. As a proof of concept, we also showed that a TeCoBot can dock by itself: a small onboard camera tracks markers on the partner robot, corrects its alignment, and locks on.

<p class="text-muted"><small>All footage is sped up.</small></p>

## Team

[Mahmud Hasan Saikot]({{ '/people/' | relative_url }}), Sydney Spiegel, [Sudheera Akalanka Kariyawasam]({{ '/people/' | relative_url }}), [Andrew Stefka]({{ '/people/' | relative_url }}), [Josh Chrisler]({{ '/people/' | relative_url }}), and [Jianguo Zhao]({{ '/people/' | relative_url }}). The work is published in _Nature Machine Intelligence_ {% cite saikot2026tecobot %}.
