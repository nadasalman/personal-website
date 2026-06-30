---
layout: page
title: Swarm Robotics — PDE-Based Motion Planning
description: >
  Diplôme d'Ingénieur graduation project — full hardware build of a 15-robot swarm (7×7 cm each) and a novel fluid-dynamics PDE path planner, benchmarked against APF and graph-based methods over 2000 experiments.
img: assets/img/swarm_project/swarm_robot_photo.png
importance: 6
category: research
---

## Context

Graduation project for the **Diplôme d'Ingénieur en Mécatronique, Université de Lattaquié** *(Sep 2020 – Jul 2021)*. The goal was to develop a computationally efficient, collision-free path planner for a fleet of non-holonomic robots, and to validate it on a custom-built physical swarm platform.

## What Was Built

- **15 differential-drive robots designed and assembled from scratch** — 7×7 cm footprint, custom PCB, onboard motor drivers, encoders and power management
- **Centralised ROS control** — overhead stereo camera provides position feedback for all agents; host computer runs the planner and dispatches velocity commands
- **PDE-based path planner** — solves the steady-state Navier-Stokes equations numerically to generate a smooth velocity vector field; robots follow the field gradient to reach their goals with no local minima and guaranteed path-finding

<div class="row mt-3">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/swarm_project/swarm_robot_photo.png" title="Assembled swarm robot (7×7 cm)" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/swarm_project/swarm_heatmap.png" title="Performance heatmap — PDE vs APF vs Graph over 2000 experiments" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Left: one of the 15 assembled robots. Right: route performance metric across 2000 simulation experiments in 20 maps — hotter colours indicate worse performance, black cells indicate planner failure. The PDE planner records zero failures across all runs.
</div>

## Key Results

- **0 path-planning failures** across 2000 experiments (20 maps × 100 start/goal pairs)
- Outperformed both APF (local minima failures) and graph-based search (lower path quality scores) across all map configurations
- Produced smooth, curvature-continuous paths directly executable by the non-holonomic robots
- Full working swarm platform delivered: hardware, firmware, ROS stack and planner integrated and validated

## Technologies

`ROS` · `C++` · `Python` · `MATLAB` · `SolidWorks` · `Custom PCB` · `Stereo camera` · `Navier-Stokes PDE` · `Numerical simulation` · `Linux`
