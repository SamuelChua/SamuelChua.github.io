---
layout: project-detail
title: Wifi-Seeing Camera
permalink: /projects/wifi-camera/
category: Wireless Sensing
summary: Making WiFi signals visible by combining directional radio measurements with camera imagery.
---

<img class="project-media" src="{{ '/assets/img/projects/wifi-camera.jpg' | relative_url }}" alt="WiFi camera prototype with a directional antenna, webcam, servo mechanism, and Arduino">

## Aim

This project scans for WiFi signals and overlays their measured strength on a camera image, giving a visual indication of where signal sources are located.

## Approach

A software defined radio and directional Yagi antenna collect radio measurements while an Arduino-controlled servo moves the antenna. Python and GNU Radio coordinate signal processing and data collection, connecting the radio measurements to the camera view.

The prototype brings together mechanical fabrication, motor control, and digital signal processing to explore the spatial distribution of wireless signals.

[Code](https://github.com/SamuelChua/Wifi-Cam) 