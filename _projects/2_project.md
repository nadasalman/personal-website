---
layout: page
title: ROS2 Distributed Architecture for Exoskeleton
description: Design and implementation of a modular, distributed ROS2 software stack connecting motor control, sensors and assistance algorithms.
img: assets/img/project2.png
importance: 2
category: research
---

## Context

Carried out as part of my PhD at **LISV — Université Paris-Saclay (2022–2026)**. The exoskeleton required a robust, real-time software backbone capable of synchronising motor commands, EMG data, force measurements and high-level control logic across multiple processors.

## Architecture

- **Raspberry Pi** (embedded) running low-level motor and sensor nodes via CAN Bus
- **Host workstation** running high-level control, visualisation and logging nodes
- Inter-machine communication via **ROS2 DDS over Ethernet**

## Responsibilities

- Implemented ROS2 nodes in **C++ and Python** for motor control, sensor acquisition and assistance logic
- Configured multi-machine ROS2 discovery and DDS tuning for stable real-time operation
- Integrated EMG and force sensor data streams into the control loop
- Built **rosbag2** recording pipelines for all experimental sessions
- Developed RViz2/rqt dashboards for real-time monitoring and debugging

## Key Results

- Stable and modular software platform supporting all experimental phases of the PhD
- Reproducible data acquisition pipeline (rosbag2) used across 5+ user studies
- Clean separation between real-time control (C++) and data-analysis layers (Python)

## Technologies

`ROS2` · `C++` · `Python` · `Raspberry Pi` · `CAN Bus` · `EtherCAT` · `Linux` · `rosbag2` · `rqt` · `RViz2`
