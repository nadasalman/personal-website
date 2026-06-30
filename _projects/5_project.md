---
layout: page
title: Adaptive EMG-Based Control of a Haptic Interface
description: Master project — real-time EMG-driven adaptive impedance controller for a rehabilitation haptic device (ICube lab, 2022).
img: assets/img/project5.png
importance: 5
category: research
---

## Context

Master project (M2 Medical Robotics) at **ICube Laboratory, Université de Strasbourg (Feb–Sep 2022)**. The goal was to adapt the speed of a haptic rehabilitation task automatically, based on the user's current muscular effort measured via surface EMG — providing less resistance when the user is fatigued and more challenge when they are stronger.

## Responsibilities

- **EMG acquisition** — multi-channel real-time acquisition via the device's analogue inputs
- **Signal processing chain** — 4th-order Butterworth bandpass filter (20–450 Hz), linear envelope, MVC normalisation
- **Event detection** — CuSum (CUSUM) change-point algorithm for reliable muscle activation onset/offset detection
- **Control implementation** — impedance controller developed in C++ under **ROS**, interfaced with the haptic device via **EtherCAT** and **Maxon EPOS4** motor drives
- **Experimental parameter tuning** — gain selection via pilot trials with healthy participants
- **User study** — designed protocol, ran sessions, analysed outcomes

## Key Results

- Reliable real-time detection of muscle activation events across all participants
- Automatic adaptation of haptic task speed to user EMG level
- Full EMG-to-command pipeline integrated and validated in the robotic system
- Successful user validation on healthy participants

## Technologies

`ROS` · `ROS Control` · `C++` · `Linux` · `EtherCAT` · `Maxon Motors` · `EPOS4` · `rqt` · `rosbag` · `Impedance control` · `Python` · `MATLAB`
