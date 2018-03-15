# Week2 summarization-1
### Learning From Noisy Large-Scale DatasetsWith Minimal Supervision[[1]](https://vision.cornell.edu/se3/wp-content/uploads/2017/04/DeepLabelCleaning_CVPR.pdf) <br>
*Veit at al. CVPR 2017*

## Goal 
Train a **multi-label image classifier** using a large dataset with relatively **noisy labels**, where additionally a small subset of the dataset has human verified labels available.

## Novelties
Instead of fine-tuning on pre-trained model (The author argues that the performance is not good enough), the proposed approach trains a network from scratch using noisy labels and then facilitates a small set of clean labels to fine-tune the network.
## Contribution
1. Introduce a multi-task framework for multilabel image classification that facilitates small sets of clean annotations in conjunction with massive sets of noisy annotations.
2. Provide a first benchmark on the recently released Open Images Dataset[[2]](https://github.com/openimages/dataset).
3. The proposed learning approach is more effective in leveraging small labeled data than traditional fine-tuning.
