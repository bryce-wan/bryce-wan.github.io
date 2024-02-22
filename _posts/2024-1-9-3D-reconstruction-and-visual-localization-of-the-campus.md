---
layout: post
title:  "3D Reconstruction and Visual Localization in the Campus"
info: "Used hloc to reconstruct the 3D model (sparse) of a building in our campus, and implemented the visual localization function with pixloc by training our own model."
tech: "Python, COLMAP"
type: Term Project
---

## Introduction

Term project (independent work) for the course Introduction to Computer Vision (2023 Spring & Summer), Zhejiang University

## Supervisor

Prof. [**Xiaowei Zhou**](https://www.xzhou.me)

## Project Description

In this project, the aim is to reconstruct a building in our campus using SfM and then complete the visual localization task based on query images (to get a 6 DOF camera pose with the 3D model reconstructed and the query image). I first took a large number of photos of a building on campus during the day and used these photos to reconstruct a 3D sparse model of the building using [**hloc**](https://github.com/cvg/Hierarchical-Localization) (a hierarchical localization toolbox). During the reconstruction process, I used several different algorithms for the reconstruction and compared the results. Next, I took many photos of the building at night with low brightness and used these photos for visual localization. I did this first using the localization algorithms already implemented in hloc, and then I trained our own neural network based on [**pixloc**](https://github.com/cvg/pixloc) for end-to-end visual localization testing. Ultimately, we compared these two visual localization schemes (mainly measured by the mean reprojection error).

## Techique

I complete the whole job mainly with python. I used **hloc** to reconstruct the 3D model of the building, and implemented the visual localization function with **pixloc** by training our own model.

## Duration

It takes about one month to complete the project (in Dec 2023).

## Result

- Here are the visualization results of the keypoints in the database images.

<center>

<table><tr>
<td><img src="/assets/demo/3D_reconstruction/kps1.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/kps2.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/kps3.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/kps4.png" width="800" border="1"></td>
</tr></table>

blue: visible in the 3D model &nbsp; &nbsp; red: invisible in the 3D model
</center>

<br/>

<center>

<table><tr>
<td><img src="/assets/demo/3D_reconstruction/depth1.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/depth2.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/depth3.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/depth4.png" width="800" border="1"></td>
</tr></table>

estimated depth of the keypoints

</center>

- Here are the reconstructed 3D model and the estimated camera poses.

<!-- 3d model -->
<center>

<table><tr>
<td><img src="/assets/demo/3D_reconstruction/reconstruction_1.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/reconstruction_2.png" width="800" border="1"></td>
</tr></table>

<table><tr>
<td><img src="/assets/demo/3D_reconstruction/reconstruction_3.png" width="800" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/reconstruction_4.png" width="800" border="1"></td>
</tr></table>

sparse 3D reconstruction model
</center>

<br/>

<!-- camera poses -->
<center>

<img src="/assets/demo/3D_reconstruction/reconstruction_camera.png" width="800" alt="3D reconstruction model and estimated camera poses" border="1">

visualization of the camera poses
</center>

- The visual localization results of the pixloc are shown below. For each query image, we first find the closest image in the database (which has a known camera pose) and obtain the relative pose relation. At this point we also get the absolute camera pose of the query image. The animation exhibits the relative pose of the query image with respect to the reference image.

<center>

<table><tr>
<td><img src="/assets/demo/3D_reconstruction/pixloc_1.png" width="450" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/pixloc_2.png" width="450" border="1"></td>
</tr></table>

green: keypoints in the reference image &nbsp; &nbsp; red: keypoints in the query image &nbsp;

</center>

<br/>

<center>

<video controls="controls" width="400">
    <source src="/assets/demo/3D_reconstruction/pixloc_1.mp4" type="video/mp4">
</video>

<video controls="controls" width="400">
    <source src="/assets/demo/3D_reconstruction/pixloc_2.mp4" type="video/mp4">
</video>
<br/>

Mapping and transformation of the keypoints
</center>

<br/>

<center>

<img src="/assets/demo/3D_reconstruction/pixloc_vis_1.png" width="800" border="1">
<img src="/assets/demo/3D_reconstruction/pixloc_vis_2.png" width="800" border="1">

visualization of the camera poses

</center>

- The charts below show the mean reprojection error and the time to localize a query image on the basis of 3D models reconstructed using different algorithms (the independent variable is the tolerance for error).

<center>

<table><tr>
<td><img src="/assets/demo/3D_reconstruction/mre_compare.png" border="1"></td>
<td><img src="/assets/demo/3D_reconstruction/loc_time_compare.png" border="1"></td>
</tr></table>
left: mean reprojection error &nbsp; &nbsp; right: time cost
</center>

- The confidence of the visual localization result is presented in the form of a heat map.

<center>

<video controls="controls" width="600">
    <source src="/assets/demo/3D_reconstruction/confidence.mp4" type="video/mp4">
</video>

</center>
