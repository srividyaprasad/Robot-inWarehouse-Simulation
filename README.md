# Robot-in-Warehouse-Simulation

This repository is a Gazebo simulation of a Turtlebot3 robot model with realistic IMU and Wheel Encoder plugins spawned in a Warehouse for our research.

## Overview

This project integrates:
- **Robot Model**: [Turtlebot3](https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git)
- **Robot Model with Sensor Noise Plugins**: [HighFidelitySensorModels](https://github.com/hlkbyrm/HighFidelitySensorModels/)
- **Warehouse World**: [AWS RoboMaker Small Warehouse World](https://github.com/aws-robotics/aws-robomaker-small-warehouse-world)

## Dependencies

    sudo apt install ros-noetic-dynamixel-sdk
    sudo apt install ros-noetic-turtlebot3-msgs
    sudo apt install ros-noetic-turtlebot3

## Setup Instructions

Follow these steps to set up

    cd catkin_ws/src
    git clone https://github.com/srividyaprasad/Robot-inWarehouse-Simulation
    cd ..
    catkin_make
    source devel/setup.bash

Run normal Turtlebot robot in Warehouse

    roslaunch turtlebot3_gazebo turtlebot_gazebo_warehouse.launch

Run realistic Turtlebot robot in Warehouse

    roslaunch turtlebot3_description_poisson turtlebot_gazebo_warehouse.launch
    rosrun turtlebot3_description_poisson sensor_uncertainty_generator.py