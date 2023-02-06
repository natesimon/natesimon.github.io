---
layout: page
title: flowdrone build guide (in-progress)
description: autonomous quadrotor control via PX4
img: assets/img/x500/X500.jpg_original
importance: 1
category: work
---

This guide walks through the design of FlowDrone, an autonomous quadrotor platform used in my research. This guide enables something very specific: **autonomous, onboard, indoor/outdoor control of a PX4 platform**. In other words, all computation and sensing is contained _onboard_ (the system does not rely on motion capture or GPS for localization). Furthermore, the custom control scripts can be written in Python or C++, and commands to the PX4 are sent over the [ROS2 bridge](https://docs.px4.io/main/en/ros/ros2_comm.html). Under this architecture, it is possible to read-in (and publish) any of the [uORB topics](https://docs.px4.io/main/en/middleware/uorb.html), as well as to publish position, velocity, acceleration, attitude, or body rate setpoints using [offboard control](https://docs.px4.io/main/en/ros/ros2_offboard_control.html).

There is a great deal of open-source content by PX4 (tutorials, pages, forum Q&A). This guide is meant to augment that content by providing a clear, descriptive build guide for one specific platform (in some sense, an "existence proof").


<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/x500/X500.jpg_original" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/x500/system_overview_freq.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Left: the FlowDrone platform in hover. Right: the system overview, as instantiated in our paper. The system consisted of a Pixhawk 4 autopilot (for low-level control), Raspberry Pi companion computer (for learning-based autonomous control in Python), and a custom MAST flow sensor with corresponding data acquisition unit (DAQ).
</div>

If you find this guide to be helpful in your research, please consider citing our [paper](https://arxiv.org/pdf/2210.05857.pdf):
```
@article{simon2022flowdrone,
  title={FlowDrone: wind estimation and gust rejection on UAVs using fast-response hot-wire flow sensors},
  author={Simon, Nathaniel and Ren, Allen Z and Piqu{\'e}, Alexander and Snyder, David and Barretto, Daphne and Hultmark, Marcus and Majumdar, Anirudha},
  journal={arXiv preprint arXiv:2210.05857},
  year={2022}
}

```

## Table of Contents
1. [Hardware](#hardware)
2. [ROS2 Bridge (C++ / Python)](#ros2-python)
3. [Offboard Control](#offboard-control)
4. [The MAST and DAQ](#mast-and-daq)
5. [Results](#results)

### Hardware <a name="hardware"></a>

The FlowDrone is based on the [Holybro X500](https://docs.px4.io/main/en/frames_multicopter/holybro_x500_pixhawk4.html) frame. We used a [Pixhawk 4](http://www.holybro.com/product/pixhawk-4/) autopilot and an 8GB [Raspberry Pi 4](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/) companion computer. In addition to the PM07 Power Module, we installed a [Matek X Class 12S Power Distribution Board](https://www.amazon.com/Distribution-FCHUB-12S-Supports-Regulators-Current/dp/B07MHKTF7F/) to provide a 5V supply to the Raspberry Pi.

### ROS2 Bridge (C++ / Python) <a name="ros2-python"></a>

The PX4 computer and firmware is optimized for speed. This optimization renders the firmware code challenging to modify directly. It is instead recommended that you use a companion computer for your custom computations, and then use a communication protocol to send (receive) data to (from) the PX4. Of the available options, we chose to use ROS2 (recommended at the time).

#### Installing ROS2 on the Raspberry Pi

First, install Ubuntu 20.04 on the Raspberry Pi ([youtube](https://www.youtube.com/watch?v=GVgMM_TFeOw)). Then, follow the ROS2 [installation instructions](https://docs.ros.org/en/foxy/How-To-Guides/Installing-on-Raspberry-Pi.html) for the Raspberry Pi.

#### Enabling the ROS2 Bridge

### Offboard Control <a name="offboard-control"></a>

### The MAST and DAQ <a name="mast-and-daq"></a>

### Results <a name="results"></a>