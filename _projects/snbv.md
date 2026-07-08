---
layout: page
title: Semantic-Aware Active Perception
description: Next-best-view planning for robotic grasping in cluttered environments.
img: /assets/img/snbv_thumbnail.png
importance: 1
category: Research
related_publications: false
---

## Overview

Robotic grasping in cluttered environments is challenging because target objects are often heavily occluded. This project presents a semantic-aware active perception framework that enables a Franka Panda robot to autonomously explore the scene, localize a target object, and execute a successful grasp without prior knowledge of the object's location.

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid
      path="assets/img/snbv.gif"
      title="Semantic-Aware Active Perception Demo"
      class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  The robot actively explores the scene before executing the final grasp.
</div>

## System Pipeline

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid
      path="assets/img/snbv_pipeline.png"
      title="System Pipeline"
      class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
  Overall pipeline of the semantic-aware active perception framework.
</div>

The framework integrates semantic perception, volumetric mapping, active viewpoint planning, and grasp planning in a closed-loop pipeline to autonomously localize and grasp occluded target objects.

## Semantic-aware Information Gain

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid
      path="assets/img/snbv_method.png"
      title="Semantic-aware Information Gain"
      class="img-fluid rounded z-depth-1" %}
  </div>
</div>

<div class="caption">
    The proposed method combines workspace-level and target-centric geometric information gain to prioritize viewpoints that reveal the target object.
</div>

## Experimental Results

The proposed framework was evaluated in both simulation and real-world experiments using a Franka Emika Panda robot.

- **Simulation:** 84% grasp success under heavy occlusion.
- **Real robot:** 10/10 success (fully occluded), 9/10 success (partially visible).

## Citation

📄 **Paper:** [_Semantic-Aware Active Perception for Next-Best-View Grasp Planning_](https://link.springer.com/article/10.1007/s12541-026-01554-0)

If you find this work useful in your research, please cite:

> Kweon, T. H., & Jeon, S. (2026). _Semantic-Aware Active Perception for Next-Best-View Grasp Planning_. International Journal of Precision Engineering and Manufacturing.

```bibtex
@article{kweon2026semantic,
  title={Semantic-Aware Active Perception for Next-Best-View Grasp Planning},
  author={Kweon, Tae Hyeon and Jeon, Soo},
  journal={International Journal of Precision Engineering and Manufacturing},
  year={2026}
}
```
