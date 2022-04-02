---
layout: single
title: Hector Quadrotor - ROS Noetic
excerpt: "Due hector quadrotor only have melodic version working, in this thread I generated a port of this dron simulator to work with ROS Noetic."
date: 2022-03-30
classes: wide
header:
  teaser: /assets/images/2022-02-26-hector-ros-noetic/gif.GIF
  teaser_home_page: true
  icon: /assets/images/rosf.png
categories:
  - ROS
  - Port
tags:
  - noetic
  - ros
  - hector
  - quadrotor
  - ubuntu 20
  - port
  - drones
---


# hector_quadrotor ported to ROS Noetic & Gazebo 11

<p align="center">
  <img src="https://raw.githubusercontent.com/RAFALAMAO/hector-quadrotor-noetic/main/imgs/dron_photo.png" width="350">
  <img src="https://raw.githubusercontent.com/RAFALAMAO/hector-quadrotor-noetic/main/imgs/dron_photo_rviz.png" width="350">
</p>

***.:: First version, please tell me the issues or help me to fix it ::.***

I took part of this from __The Construct's__ [repo](https://bitbucket.org/theconstructcore/hector_quadrotor_sim/src/master/) and YouTube [chanel](https://www.youtube.com/channel/UCt6Lag-vv25fTX3e11mVY1Q).

## Requirements

I. You need the following packages before install `hector_quadrotor_noetic`.

* unique_identifier:
    ```sh
    git clone https://github.com/ros-geographic-info/unique_identifier.git
    ```
* geographic_info:
    ```sh
    git clone https://github.com/ros-geographic-info/geographic_info.git
    ```

II. Build.
```sh
cd ~/catkin_ws && catkin_make
```

III. Clone `hector_quadrotor_noetic`.
```sh
git clone https://github.com/RAFALAMAO/hector_quadrotor_noetic.git
```

IV. Repeat step II.

## Usage

Run a simulation by executing the launch file in `hector_quadrotor_gazebo` and `hector_quadrotor_demo` packages (only these work at the momment, but you can try the other ones):

* `roslaunch hector_quadrotor_gazebo quadrotor_empty_world.launch`
* `roslaunch hector_quadrotor_demo outdoor_flight_gazebo.launch`
* `roslaunch hector_quadrotor_demo outdoor_flight_gazebo_no_rviz.launch`
* `roslaunch hector_quadrotor_demo two_drones_empty.launch`

You can control it with teleop_twist_keyboard.
* `git clone https://github.com/ros-teleop/teleop_twist_keyboard`

## Test

Here is a [video](https://www.youtube.com/watch?v=-2IWfZjqoNc) testing it:

<iframe width="560" height="315" src="https://www.youtube.com/embed/-2IWfZjqoNc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>