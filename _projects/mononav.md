---
layout: default
permalink: /mononav/
title: MonoNav
description: MAV Navigation via Monocular Depth Estimation and Reconstruction
img: assets/img/publication_preview/MonoNav_Anchor.png
importance: 1
category: work
---

<h1><center><span style="font-weight:bold;">MonoNav:</span><br>MAV Navigation via Monocular Depth Estimation and Reconstruction</center></h1>
<br>
<table style="width: 80%; max-width: 800px; margin: 0 auto;">
    <tr>
        <td style="text-align: center; width: 100px;">
            <span style="font-size: 22px; font-weight:bold;"><a href="https://natesimon.github.io/" target="_blank">Nathaniel Simon</a></span>
        </td>
        <td style="text-align: center; width: 100px;">
            <span style="font-size: 22px; font-weight:bold;"><a href="https://irom-lab.princeton.edu/majumdar/" target="_blank">Anirudha Majumdar</a></span>
        </td>
    </tr>
</table>
<td align=center style="width: 80%; max-width: 800px; margin: 0 auto; text-align: center;">
<div style="text-align: center; max-width: 200px; margin: 0 auto;">
    <p style="margin-top: 4px;"></p>
    <a href="https://irom-lab.princeton.edu/">
        <img src="../assets/img/irom_lab_logo.png" alt="IRoM" style="width: 100%;">
    </a>
</div>
<p style="margin-top: 2px;"></p>
<center><span style="font-size:20px"><a href="https://robo.princeton.edu/" target="_blank">Princeton University</a></span></center>
</td>
<br>
<table style="width: 70%; max-width: 800px; margin: 0 auto;">
    <tr>
    <td align=center width=20px><center><span style="font-size:28px">
        <a href="../../assets/pdf/MonoNav_ISER2023.pdf" target="_blank"><img src="../assets/img/PDF_file_icon.png" alt="PDF File Icon" style="max-width: 50px; height: auto;"></a></span></center>
    </td>
    <td align=center width=20px><center><span style="font-size:28px">
        <a href="https://youtu.be/msWLSfOmTpI" target="_blank"><img src="../assets/img/YouTube_full-color_icon_(2017).png" alt="Youtube Play Icon" style="max-width: 50px; height: auto;"></a></span></center>
    </td>
        <td align=center width=20px><center><span style="font-size:28px">
        <a href="https://github.com/natesimon/MonoNav/" target="_blank"><img src="../assets/img/GitHub_Invertocat_Logo.png" alt="Github Icon" style="max-width: 50px; height: auto;"></a></span></center>
    </td></tr>
    <tr>
    <td align=center width=20px><center><span style="font-size:28px"><a href="../../assets/pdf/MonoNav_ISER2023.pdf">[PDF]</a></span></center></td>
    <td align=center width=20px><center><span style="font-size:28px"><a href="https://youtu.be/kVoIIsdoQR4">[Video]</a></span></center></td>
    <td align=center width=20px><center><span style="font-size:28px"><a href="https://github.com/natesimon/MonoNav/">[Code]</a></span></center></td>
    </tr>
</table>
<br>
<table style="width: 80%; max-width: 800px; margin: 0 auto;">
    <tr>
        <td style="text-align: center; width: 20%; vertical-align: top;">
            <a href="https://thenounproject.com/icon/award-1976316/" target="_blank"><img src="../assets/img/mononav/noun-award-1976316.png" alt="Image Description" style="max-width: 50px; height: auto;"></a>
        </td>
        <td style="width: 80%;">
            <p style="font-size: 20px;">
                <b>Best Paper:</b> <a href="https://wp.nyu.edu/workshopiros2023superautonomy/">Learning Robot Super Autonomy</a> Workshop at IROS 2023.
            </p>
        </td>
    </tr>
    <tr>
        <td style="text-align: center; width: 20%;">
            <a href="https://thenounproject.com/icon/binoculars-5031330/" target="_blank"><img src="../assets/img/mononav/noun-binoculars-5031330.png" alt="Image Description" style="max-width: 50px; height: auto;"></a>
        </td>
        <td style="width: 80%;">
            <p style="font-size: 20px;">
                <b>To appear:</b> <a href="https://iser2023.org/">ISER 2023</a>.
            </p>
        </td>
    </tr>
</table>
<br>
<center><div style="font-size: 20px; width: 100%; max-width: 800px; margin: 0 auto;">
    <b>Warning:</b> This is a research preview. Evaluation against state of the art monocular navigation baselines is underway. Stay tuned!
</div></center>
<div class="row mt-3">
    <div class="col-sm col-12 mt-3 mt-md-0 d-flex justify-content-center">
        <div class="embed-responsive embed-responsive-16by9" style="width: 100%; max-width: 800px; margin: 0 auto;">
            <iframe class="embed-responsive-item rounded z-depth-1" src="https://www.youtube.com/embed/msWLSfOmTpI"></iframe>
        </div>
    </div>
</div>
<br>
<div style="font-size: 18px; width: 100%; max-width: 800px; margin: 0 auto; text-align:justify">
<b>Abstract:</b> The small form factor of micro aerial vehicles (MAVs) makes them highly appealing for autonomous inspection, exploration, and mapping of constrained indoor environments. However, a major challenge with deploying the smallest of these platforms (< 100 g) is their inability to carry sensors that provide high-resolution metric depth information (e.g., LiDAR or stereo cameras). Equipped only with a monocular camera and inertial measurement unit, such systems currently rely on  end-to-end learning or heuristic approaches that directly map images to control inputs, and struggle to fly fast in unknown environments. In this work, we ask the following question: using only a monocular camera and offboard compute, can we create metrically accurate depth maps to leverage the powerful path planning and navigation approaches employed by larger state-of-the-art robotic systems to achieve robust autonomy in unknown environments? 
We present MonoNav: a fast 3D reconstruction and navigation stack for MAVs that leverages recent advances in depth prediction neural networks to enable metrically accurate 3D scene reconstruction from a stream of monocular images and poses. MonoNav uses off-the-shelf pre-trained monocular depth estimation and fusion techniques to construct a map, then searches over motion primitives to plan a collision-free trajectory to the goal. In extensive hardware experiments, we demonstrate how MonoNav enables the Crazyflie (a 37 g MAV) to navigate fast (0.5 m/s) in cluttered indoor environments.
</div>
<br>
<center><h2>MonoNav System Overview</h2></center>
<br>
<div style="font-size: 18px; width: 100%; max-width: 800px; margin: 0 auto; text-align:justify">
    MonoNav uses pre-trained depth-estimation networks (<a href="https://github.com/isl-org/ZoeDepth">ZoeDepth</a>) to convert RGB images into depth estimates, then fuses them into a 3D reconstruction using <a href = "http://www.open3d.org/">Open3D</a>. MonoNav then selects from motion primitives to navigate collision-free to a goal position.
</div>
<div style="text-align: center; max-width: 800px; margin: 0 auto;">
    <p style="margin-top: 4px;"></p>
    <a href="../../assets/img/mononav/MonoNav_System.png">
        <img src="../../assets/img/mononav/MonoNav_System.png" alt="MonoNav System" style="width: 100%;">
    </a>
</div>
<br>
<center><h2>Results: Reconstruction and Planning</h2></center>
<div style="font-size: 18px; width: 100%; max-width: 800px; margin: 0 auto; text-align:justify">
    In 15 runs across 10 unique indoor settings, (six of which are shown below), MonoNav navigates successfully and avoids obstacles. Of the 15 runs, MonoNav crashed once (Hall 4), and was prematurely terminated once (Hall 1). In both cases, MonoNav turned into a wall or dead-end that was previously occluded and thus not perceived as an obstacle (and is hence missing from the reconstruction). Such behavior can be fixed by careful tuning of the planning module.
</div>
<div style="text-align: center; max-width: 800px; margin: 0 auto;">
    <p style="margin-top: 4px;"></p>
    <a href="../../assets/img/mononav/MonoNavReconstructions.png">
        <img src="../../assets/img/mononav/MonoNavReconstructions.png" alt="MonoNav Reconstructions" style="width: 100%;">
    </a>
</div>
