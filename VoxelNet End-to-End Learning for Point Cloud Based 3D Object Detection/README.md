# Week10 summarization
### VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection [[1]](https://arxiv.org/pdf/1711.06396.pdf)

## Goal
Use an end-to-end trainable model for 3D object detection and discard the needs for hand-crafted feature.

## Background
1. Point cloud based 3D object detection is an important component of a variety of real-world 
applications, such as autonomous navigation, housekeeping robots, and augmented/virtual reality.
2. Point clouds are sparse and many approaches manually crafted feature representation for it.
3. PointNet, an end-to-end Deep neural network  was proposed.
4. Region proposal network (RPN) is a highly optimized algorithm for efficient object detection.

## Contribution
1. Propose an end-to-end trainable deep architecture for point-cloud-based 3D object detection.
2. Propose an efficient method for VoxelNet implementation.
3. The proposed model produces state-of-the-art results in LiDAR-based car, pedestrian, and cyclist detection
benchmarks.
