---
layout: page
title: VLM-Based Robot Policy Verification
description: Using vision-language models to verify and refine robotic manipulation tasks.
img: /assets/img/vlm_success.png
importance: 3
category: Research
related_publications: false
---

## Overview

This project explores using vision-language models as high-level evaluators for robotic policies. Given wrist camera observations after task execution, the VLM verifies whether the robot successfully completed the intended manipulation task and generates feedback that can be used to refine task instructions.

## Project Scope

- Collected teleoperation trajectories for VLA fine-tuning.
- Fine-tuned OpenPI 0.5 for robotic manipulation tasks.
- Developed a VLM-based policy verification prototype using Qwen2.5-VL.

<div class="row justify-content-center">
  <div class="col-md-6 mt-3">
    {% include figure.liquid
      path="assets/img/vlm_success.png"
      title="Successful Grasp"
      class="img-fluid rounded z-depth-1" %}
  </div>

  <div class="col-md-6 mt-3">
    {% include figure.liquid
      path="assets/img/vlm_fail.png"
      title="Failed Grasp"
      class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
Qwen2.5-VL verifies grasp execution from wrist camera observations, correctly distinguishing successful and failed grasp attempts.
</div>
