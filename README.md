# Steering angle based on camera feed

This project implements an autonomous road-following system using the NVIDIA Jetson Orin and ROS2 (Robot Operating System). The system leverages deep learning models to process real-time video feeds from a model vehicle mounted camera, predicting steering angles based on the road's appearance, enabling autonomous navigation. These models are trained for a model city at the moment and will only work in this specific map.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Training the Model](#training-the-model)

## Introduction

This project showcases the deployment of a deep learning-based autonomous road-following system on the NVIDIA Jetson Orin. It captures real-time video from a camera attached to the vehicle, processes these frames, and employs a trained neural network to estimate the steering angle according to the road's visual cues. These steering commands are then relayed to the vehicle, allowing it to autonomously follow the road.

## Installation

### Step 1: Clone the Repository

First, clone the repository to your workspace 

### Step 2: Build the Package

Upon successful completion of the cloning process, go to workspace and build the package by using the colcon command.

### Step 3: Source the Workspace
Once the build process finishes, you'll have to source the workspace to make it accessible for ROS2.
```shell
source install/setup.bash
```

### Step 4: Run the node
You can now launch the jetracer node:

```shell
 ros2 run jetracer2ros jetracer_ros_node 
 ```
### Step 5: Run the realsense_camera 
In a new terminal, launch the realsense_camera node:

```shell
 ros2 launch realsense2_camera rs_launch.py 
 ```

## Training the model

Open the training notebook from the notebook folder and follow the steps to train your model. The notebooks include data preprocessing, model training, and validation.
