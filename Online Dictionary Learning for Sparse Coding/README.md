# Week3 summarization
### Online Dictionary Learning for Sparse Coding[[1]](https://www.di.ens.fr/~fbach/mairal_icml09.pdf)<br>
*Mairal et al. ICML 2009*

## Background
Sparse coding—that is, modelling data vectors as sparse linear combinations of basis elements—is widely used in machine learning, neuroscience, signal processing, and statistics. 
Spaqrse coding can be used to:
1. Denoising
2. Representation of data
3. Signal econstruction

in an effective way.


## Goal
Learn dictionary (the basis set) based on proposed new online optimization algorithm for faster and better performance on large scale datasets.

## Novelties
1. Propose Online Dictionary Learning 
2. Use dictionary learning for image restoration on large-scale data, [Berkeley segmentation dataset](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/bsds/).

## Contribution
Contrary to classical first-order stochastic gradient descent, the dictionary learning method does not require explicit learning rate tuning and minimizes a sequentially quadratic local approximations of the expected cost.
>>>>>>> 9815c47c37e8583d8e4552a9748c1cc651d9a171