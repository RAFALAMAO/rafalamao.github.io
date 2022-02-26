---
layout: single
title: Hector Quadrotor Ported - ROS Noetic
excerpt: "A port of hector quadrotor for ROS Noetic with Gazebo 11 in Ubuntu 20."
date: 2022-03-25
classes: wide
header:
  teaser: /assets/images/htb-writeup-unbalanced/unbalanced_logo.png
  teaser_home_page: true
  icon: /assets/images/ros.png
categories:
  - Robotic
tags:  
  - ROS
  - Noetic
  - Dron
  - Gazebo 11
---

## hector_quadrotor ported to ROS Noetic & Gazebo 11


***.:: First version, please tell me the issues or help me to fix it ::.***

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
