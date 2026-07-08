---
layout: page
title: VLM-Distilled Next-Best-View Planning
description: Learning active perception policies from vision-language model preferences.
img: /assets/img/prefnbv_topview.gif
importance: 2
category: Research
related_publications: false
---

## Overview

This project investigates learning next-best-view (NBV) policies for robotic grasping from offline vision-language model (VLM) preferences. Rather than querying a VLM during deployment, a lightweight NBV policy is trained to imitate VLM viewpoint rankings, enabling efficient active perception.

<div class="row justify-content-center">
  <div class="col-md-6 mt-3">
    {% include figure.liquid
      path="assets/img/prefnbv_topview.gif"
      title="Initial view"
      class="img-fluid rounded z-depth-1" %}
  </div>

  <div class="col-md-6 mt-3">
    {% include figure.liquid
      path="assets/img/prefnbv_starttop.gif"
      title="Top view"
      class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
The learned NBV policy selects informative viewpoints from different initial camera configurations.
</div>

## System Overview

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid
      path="assets/img/prefnbv_overview.png"
      title="System Overview"
      class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Overview of the proposed framework. During offline training, a VLM generates viewpoint preference labels for training the proposed NBV policy. During deployment, the trained policy selects informative viewpoints in real time without VLM queries.
</div>

The proposed framework consists of three stages: (1) simulation data collection, (2) VLM-based preference learning, and (3) real-time deployment. A lightweight NBV policy is trained from offline VLM preferences and replaces expensive online VLM reasoning during robotic grasping.

## VLM Preference Learning

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid
      path="assets/img/prefnbv_labeling.png"
      title="VLM Preference Learning"
      class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
The VLM evaluates candidate viewpoints from the current observation and selects the most informative next view for robotic grasping.
</div>

During offline training, GPT-4o ranks candidate viewpoints according to how well they reveal graspable regions of the target object. These viewpoint preferences are used to train the proposed NBV policy, eliminating the need for VLM queries during deployment.

## Experimental Results

The proposed framework was evaluated in simulation using a Franka Emika Panda robot.

- **Simulation:** 79% grasp success.
- **Runtime:** 2.6× faster view selection than Information Gain-based NBV.
- **Inference:** No VLM queries required during inference.

## Status

Manuscript in preparation.
