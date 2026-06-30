---
layout: page
title: Real-Time Load Estimation from EMG
description: Online load estimation using surface EMG to automatically adapt exoskeleton assistance — fuzzy-logic approach with per-user calibration.
img: assets/img/project3.png
importance: 3
category: research
related_publications: true
---

## Context

Developed during my PhD at **LISV (2022–2026)**. One of the core challenges in assistive exoskeletons is knowing *how much* the user needs: estimating the weight of a held object in real time without dedicated load cells at the hand. The solution exploits the relationship between muscle activity (EMG) and external load.

## Approach

1. **Signal acquisition** — 4-channel surface EMG from biceps brachii and anterior deltoid
2. **Preprocessing** — Butterworth bandpass filtering (20–450 Hz), RMS and variance feature extraction
3. **Fuzzy-logic estimator** — maps EMG features to load estimate with linguistically interpretable rules
4. **Per-user calibration** — 2-minute calibration session maps individual muscle patterns to reference loads
5. **Online adaptation** — estimated load fed in real time to the gravity-compensation algorithm

## Key Results

- Reliable online load estimation over 0–3 kg range during elbow flexion/extension
- Automatic assistance adaptation without any physical load sensor at the hand
- Validated on healthy participants in flexion/extension tasks

## Technologies

`Python` · `MATLAB` · `Surface EMG` · `Digital signal processing` · `Fuzzy logic` · `ROS2`

---

{% cite salman2024adaptive %}
