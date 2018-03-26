# Week2 summarization-2
### Learning Deep Object Detectors from 3D Models[[1]](http://www.karimali.org/publications/PSAS_ICCV15.pdf)<br>
*Peng et al. ICCV 2016*
## Goal
Gain more insights about the 3D synthetic data for augmentation and use DCNN for training.
## Novelties
1. Demonstrate experiments to analyse the nature of the invariances.
2. Train a classifier on PASCAL using DCNN.
3. Propose a new method for learning object detectors for new categories that avoids the need for costly large-scale image annotation.

*Note: The article defines “cue invariance” to to be the ability of the network to extract the same high-level category information
from training images despite missing low-level cues such as object texture.*

The idea could be summzrized as following figure:
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Learning%20Deep%20Object%20Detectors%20from%203D%20Models/image/f2.png"><br>
## Contribution
1. To analyze how missing low-level cues of synthetic data affects object detection performance.
2. Shows the improved performance by using DCNN on PASCAL VOC2007 dataset.
3. Present the largest-scale evaluation of synthetic CAD training of object detectors to date.
## Technical summarizes
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Learning%20Deep%20Object%20Detectors%20from%203D%20Models/image/t1.png"><br>

1. **Synthetic Generation of LowLevel Cues:** Download models from *3D Warehouse* then adjust viewpoints, object/background color and texture. Several examples are shown on the first row of above figure.
2. **Deep Convolutional Neural Network Features:** Apply AlexNet[[2]](https://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks.pdf) and RCNN[[3]](https://arxiv.org/abs/1311.2524) for feature extraction and object detection. <br>
**AlexNet:**<br>
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Learning%20Deep%20Object%20Detectors%20from%203D%20Models/image/alexnet.png" width="520"><br>
**RCNN:**<br>
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Learning%20Deep%20Object%20Detectors%20from%203D%20Models/image/rcnn.png" width="520"><br>
3. **Analysing Cue Invariance of DCNN Features:** Create two synthetic training sets one with and one without a particular cue. Compare the model performance trained on two different set. Some results are shown in Table2 below:
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Learning%20Deep%20Object%20Detectors%20from%203D%20Models/image/t2.png">

## Conclusion
* DCNNs learn a significant amount of **invariance to texture, color and pose**, and **less invariance to 3D shape.**
* Training on synthetic images with simulated cues lead to similar performance as training on synthetic images without these cues.
* For novel categories, adding synthetic variance along these dimensions and fine-tuning the layers proved useful.
## Referene
[1] Learning Deep Object Detectors from 3D Models<br>
[2] ImageNet Classification with Deep Convolutional Neural Networks<br>
[3] Rich feature hierarchies for accurate object detection and semantic segmentation<br>
