---
sidebar_position: 2
---

# 3.2 Seeing the World: Perception and Computer Vision

A robot without sensors is blind. This chapter covers how raw pixel data is converted into semantic understanding.

## Sensors
- **RGB Camera**: Color information. Good for classification.
- **Depth Camera**: Distance information. Essential for preventing collisions.
- **LiDAR**: Exact 360-degree range finding.

## Object Detection (YOLO / SSD)
The first step of awareness is knowing *what* is around you. "There is a person at (x,y)."
We will integrate a YOLO (You Only Look Once) model node into ROS 2 to publish 2D bounding boxes.

## Semantic Segmentation
Going deeper: classifying *every pixel*. "This pixel is road, this pixel is sidewalk."
This allows the robot to understand navigable surfaces versus obstacles.

## Visual Odometry (V-SLAM)
"How have I moved?"
By tracking feature points across successive camera frames, the robot can estimate its own motion (ego-motion) even without GPS or wheel encoders.
