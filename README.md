# Robot-in-Warehouse-Simulation

This repository is a Gazebo simulation of a Turtlebot3 robot model with realistic IMU and Wheel Encoder plugins spawned in a Warehouse.

## Overview

This project integrates:
- **Robot Model with Sensor Noise Plugins**: [HighFidelitySensorModels](https://github.com/hlkbyrm/HighFidelitySensorModels/)
- **Warehouse World**: [AWS RoboMaker Small Warehouse World](https://github.com/aws-robotics/aws-robomaker-small-warehouse-world)

## Setup Instructions

Follow these steps to set up and run the simulation:

    cd catkin_ws
    git clone https://github.com/srividyaprasad/Robot-inWarehouse-Simulation
    cd ..
    catkin_make
    source devel/setup.bash
    roslaunch turtlebot3_description_poisson turtlebot_gazebo.launch
    rosrun turtlebot3_description_poisson sensor_uncertainty_generator.py
