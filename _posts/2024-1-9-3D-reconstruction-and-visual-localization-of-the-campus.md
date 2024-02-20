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

In this project, I first took a large number of photos of a building on campus during the day and used these photos to reconstruct a 3D sparse model of the building using [**hloc**](https://github.com/cvg/Hierarchical-Localization) (a hierarchical localization toolbox). During the reconstruction process, I used several different algorithms for the reconstruction and compared the results. Next, I took many photos of the building at night with low brightness and used these photos for visual localization. I did this first using the localization algorithms already implemented in hloc, and then I trained our own neural network based on [**pixloc**](https://github.com/cvg/pixloc) for end-to-end visual localization testing. Ultimately, we compared these two visual localization schemes (mainly measured by the mean reprojection error).

## Techique

I complete the whole job mainly with python. I used **hloc** to reconstruct the 3D model of the building, and implemented the visual localization function with **pixloc** by training our own model.

## Duration

It takes about one month to complete the project (in Dec 2023).

## Result

<center>
<video controls="controls">
    <source src="/assets/video/3D_reconstruction/pixloc_1.mp4" type="video/mp4">
</video>


<video controls="controls">
    <source src="/assets/video/3D_reconstruction/pixloc_2.mp4" type="video/mp4">
</video>
</center>