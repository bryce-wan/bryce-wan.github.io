---
layout: post
title:  "7-DOF space robot 'walking' on the space station"
info: "Designed a 7-DOF robot arm and solved its forward and inverse kinematics, then implemented trajectory planning algorithm using quintic polynomials to make it finally 'walk' on the walls of a space station"
tech: "Python, Matlab, CoppeliaSim"
type: Term Project
---

## Introduction

Term project (team work) for the course Bipedal Mobile Robot Technology (2023 Spring & Summer), Zhejiang University

## Supervisor

Prof. [**Chunlin Zhou**](https://person.zju.edu.cn/en/c_zhou)

## Project Description

This project aims to model a 7-DOF robotic arm, solve its forward and inverse kinematics, and implement a trajectory planning algorithm using quintic polynomials. The objective is to simulate its "walking" effect on the walls of a space station within CoppeliaSim. The robotic arm has a symmetrical structure, and the walking effect is achieved by exchanging the base and end-effector of the arm after each step.

## Role & Work

I was the leader of the team. I derived the forward and inverse kinematics of the designed robotic arm, and implemented the trajectory planning algorithm with python. Also, I was responsible for the simulation of the walking effect of the robotic arm within CoppeliaSim.

## Techique

We used matlab to derive the forward and inverse kinematics of the robotic arm, and implemented the trajectory planning algorithm with python. We used CoppeliaSim to simulate the walking effect of the robotic arm. 

## Duration

It takes about three weeks to complete the project (in Nov & Dec 2023).

## Result

<center>
<video controls="controls" width="600">
    <source src="/assets/demo/articulated_robot/articulated_robot_1.mp4" type="video/mp4">
</video>


<video controls="controls" width="600">
    <source src="/assets/demo/articulated_robot/articulated_robot_2.mp4" type="video/mp4">
</video>
</center>