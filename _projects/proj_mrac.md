---
layout: page
title: MRAC for a Two-Link Manipulator
description: Model Reference Adaptive Control (MRAC) simulation for trajectory tracking and parameter estimation of a nonlinear two-link robotic arm in MATLAB/Simulink.
img: assets/img/two_arm.png
redirect: false
importance: 1
category: Coursework
related_publications: false
---

### System Overview

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/two_arm.png" title="Two-Link Manipulator Diagram" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Two-link manipulator model with joint angles \( q_1, q_2 \), link lengths \( L_1, L_2 \), and payload \( m_p \).
</div>

---

### MRAC Simulink Model

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/simulink.png" title="MRAC Simulink Model" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Simulink implementation of the MRAC architecture showing the plant model, regressor matrix, parameter estimator, and adaptive controller.
</div>

---

### Simulation Results

#### Tracking Performance without Disturbance

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/Error_vs_time.png" title="Tracking Error" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Joint position tracking errors for \( q_1 \) and \( q_2 \) converge to zero, demonstrating successful adaptation.
</div>

#### Tracking under Disturbance

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/q1distur.png" title="q₁ tracking with disturbance" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/q2distur.png" title="q₂ tracking with disturbance" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Desired vs. actual joint trajectories under sinusoidal disturbance input \( \tau_d = \sin(20t) \).  
  The adaptive controller maintains stable tracking despite external perturbations.
</div>

---

### Key Outcomes

- Achieved accurate trajectory tracking and parameter adaptation for both joints.
- Verified stability using Lyapunov analysis.
- Demonstrated robustness against high-frequency sinusoidal disturbances.

---

**Tools:** MATLAB, Simulink  
**Course:** ME780A — System Identification & Adaptive Control
