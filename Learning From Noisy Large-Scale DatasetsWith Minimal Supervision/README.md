# Week2 summarization-1
### Learning From Noisy Large-Scale DatasetsWith Minimal Supervision[[1]](https://vision.cornell.edu/se3/wp-content/uploads/2017/04/DeepLabelCleaning_CVPR.pdf) <br>
*Veit at al. CVPR 2017*

## Goal 
Train a **multi-label image classifier** using a large dataset with relatively **noisy labels**, where additionally a small subset of the dataset has human verified labels available.

## Novelties
Instead of fine-tuning on pre-trained model (The author argues that the performance is not good enough), the proposed approach trains a network from scratch using noisy labels and then facilitates a small set of clean labels to fine-tune the network.
## Contribution
1. Introduce a multi-task framework for multilabel image classification that facilitates small sets of **clean** annotations in conjunction with **massive sets of noisy annotations**.
2. Provide a first **benchmark** on the recently released **Open Images Dataset**[[2]](https://github.com/openimages/dataset).
3. The proposed learning approach is more effective in **leveraging small labeled data** than traditional fine-tuning.

## Promising applications
Since the author states that the structure in the label space could be implicitly learned by the method, I think delving in the structure might be insteresting. For example, by looking up the connection of each term in labels, we probably can generate high-level semantic concept from image.

## Technical summarizes
**The proposed networks not only predict the label but also help filtering out noisy label. Figure1 below shows its concept.**
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Learning%20From%20Noisy%20Large-Scale%20DatasetsWith%20Minimal%20Supervision/image/f1.png" width="420">

The network consists of two sub-module:
1. The label cleaning network: Given noise label and visual feature, output cleaned label
2. The multi-label classifier: Given cleaned label and visual feature, output predicted label
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Learning%20From%20Noisy%20Large-Scale%20DatasetsWith%20Minimal%20Supervision/image/f2.png" >
