# Week10 summarization
### VoxelNet: End-to-End Learning for Point Cloud Based 3D Object Detection [[1]](https://arxiv.org/pdf/1711.06396.pdf)

## Goal
Use an end-to-end trainable model for 3D object detection and discard the needs for hand-crafted feature.
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/VoxelNet%20End-to-End%20Learning%20for%20Point%20Cloud%20Based%203D%20Object%20Detection/images/f0.png" width="420">
## Background
1. Point cloud based 3D object detection is an important component of a variety of real-world applications, such as autonomous navigation, housekeeping robots, and augmented/virtual reality.
2. Point clouds are sparse and many approaches manually crafted feature representation for it.
3. PointNet, an end-to-end Deep neural network  was proposed.
4. Region proposal network (RPN) is a highly optimized algorithm for efficient object detection.

## Contribution
1. Propose an end-to-end trainable deep architecture for point-cloud-based 3D object detection.
2. Propose an efficient method for VoxelNet implementation.
3. The proposed model produces state-of-the-art results in LiDAR-based car, pedestrian, and cyclist detection benchmarks.

## Techincal summaries
#### VoxelNet architecture:

<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/VoxelNet%20End-to-End%20Learning%20for%20Point%20Cloud%20Based%203D%20Object%20Detection/images/f1.png">

The overview of the prposed model is shown above. Basically, it's consist of three module, i.e., Voxel feature encoding layer, Convolutional middle layers and Region proposal network:

* Voxel feature encoding layer:<br>
VFE layers combine combine point-wise features with a locally aggregated feature. Stacking multiple VFE layers allows learning complex features for characterizing local 3D shape information.<br>
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/VoxelNet%20End-to-End%20Learning%20for%20Point%20Cloud%20Based%203D%20Object%20Detection/images/f2.png" width="520"><br>


* Convolutional middle layers:<br>
The convolutional middle layers aggregate voxel-wise features within a progressively expanding receptive field, adding more context to the shape description. Conv3D layers are used.

* modified RPN:<br>
The RPN is fed with feature maps from convolutional middle layers and the learning targets are (1) a probability score map and (2) a
regression map. THe architecture is shown below:<br>

<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/VoxelNet%20End-to-End%20Learning%20for%20Point%20Cloud%20Based%203D%20Object%20Detection/images/f3.png" width="720"><br>

#### Loss function:
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/VoxelNet%20End-to-End%20Learning%20for%20Point%20Cloud%20Based%203D%20Object%20Detection/images/f4.png" width="420"><br>
*L*cls stands for binary cross entropy loss and *L*reg is the regression loss with SmoothL1 function.
