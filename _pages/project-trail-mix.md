---
layout: project-detail
title: "Trail Mix: Multi-Robot Coordination"
permalink: /projects/trail-mix/
category: Robotics
---

The project aims to coordinate four robots across two assembly lines to prepare and serve custom trail mix orders. The system connects customer orders, task scheduling, perception, and robot control so robots can pick up cups, dispense ingredients, exchange cups at turntables, mix, and serve the finished orders.

### Shared communication layer

I led the ROS communication layer that lets these components work together. Custom message definitions and a shared Python interface, `TrailMixInterface`, give teams a consistent way to exchange commands, world state, and execution feedback. Message validation and publish-rate monitoring help catch integration errors, while status and failure messages let the scheduler track progress and respond when tasks fail.

[View code and README](https://github.com/SamuelChua/TrailMixMultiRobot)

### Demo

<video class="project-media" controls playsinline preload="metadata" poster="{{ '/assets/img/projects/trail-mix-demo.jpg' | relative_url }}" aria-label="Trail mix robot assembly line demonstration">
  <source src="{{ '/assets/video/trail-mix-demo.mp4' | relative_url }}" type="video/mp4">
  Your browser does not support embedded video. <a href="{{ '/assets/video/trail-mix-demo.mp4' | relative_url }}">Download the demo</a>.
</video>

<p class="project-caption">Robots operating at the ingredient and cup-handling stations.</p>

<figure>
  <img class="project-media" src="{{ '/assets/img/projects/trail-mix-system.jpg' | relative_url }}" alt="Four robot arms arranged across two trail mix assembly lines during the classroom demonstration" loading="lazy" width="1600" height="1200">
  <figcaption class="project-caption">The four-robot system during the final project demonstration.</figcaption>
</figure>
