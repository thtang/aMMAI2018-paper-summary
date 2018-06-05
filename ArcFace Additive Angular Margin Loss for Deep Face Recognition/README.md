# Week12 summarization
### ArcFace: Additive Angular Margin Loss for Deep Face Recognition[[1]](https://arxiv.org/pdf/1801.07698.pdf)
*Jiankang Deng, Jia Guo, Stefanos Zafeiriou, arXiv 2018*

## Goal
Propose a loss function to make the exist models' performance beyond cutting-edge.
## Background
* To enhance the discriminative power of the Softmax loss, multiplicative angular margin [2] and additive
cosine margin [3] incorporate angular margin and
cosine margin into the loss functions, respectively.
* Three attributes differ DNN face recognition methods: (1) Training dataset (2) Network architecture (3)Loss functions.
* **Data**, **network** and **loss**, have a high-to-low influenceon the performance of face recognition models.
## Contribution
1. Refined the largest public available training dataset (MS1M) and test dataset (MegaFace).
2. Explored different network settings and analysed the trade-off between accuracy and speed.
3. Proposed a geometrically interpretable loss function called ArcFace, which obtained state-of-the-art performance on the MegaFace dataset in a totally reproducible way.
## Technical summarizes

**The original softmax loss**:<br>
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/ArcFace%20Additive%20Angular%20Margin%20Loss%20for%20Deep%20Face%20Recognition/images/f1.png" width=320><br>


Then the target logit is replaced as follows:<br>
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/ArcFace%20Additive%20Angular%20Margin%20Loss%20for%20Deep%20Face%20Recognition/images/f2.png" width=220><br>
where <img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/ArcFace%20Additive%20Angular%20Margin%20Loss%20for%20Deep%20Face%20Recognition/images/f3.png" width=60> by L2 normalization.<br>

**The Additive Angular Margin loss**:<br>
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/ArcFace%20Additive%20Angular%20Margin%20Loss%20for%20Deep%20Face%20Recognition/images/f4.png" width=420><br>
*s* is the hypersphere radius and *m* is angular margin.

**Geometrical interpretation of the proposed method:**<br>
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/ArcFace%20Additive%20Angular%20Margin%20Loss%20for%20Deep%20Face%20Recognition/images/f5.png" width=420>
## Reference
[[1]](https://arxiv.org/pdf/1801.07698.pdf) ArcFace: Additive Angular Margin Loss for Deep Face Recognition.<br>
[[2]](http://openaccess.thecvf.com/content_cvpr_2017/papers/Liu_SphereFace_Deep_Hypersphere_CVPR_2017_paper.pdf) Sphereface: Deep hypersphere embedding for face recognition.<br>
[[3]](https://ieeexplore.ieee.org/document/8331118/) Additive margin softmax for face verification.
