# Week4 summarization
### A Hybrid Neural Network-Latent Topic Model[[1]](https://cs.nyu.edu/~wanli/wan-zhu-fergus12.pdf)<br>
*Li Wan et al. JMLR 2012*

## Background
Probabilistic graphical models and neural networks are the two prevalent types of belief network in machine learning.
1. For probabilistic graphical models, explicit variables are linked in a sparse dependency structure and could be specified using domain knowledge.
2. Neural Network, on the other hand, learns implicit meaning and are densely connected.

## Contribution
1. This paper proposes a model that combines a deep neural nework (two layers in fact) with a lantent topic model (LDA).
2. Propose a novel way of transforming the graphical model so that the whole network could be trained jointly.
3. Demonstrate the model on computer vision setting, scene classification.

## Technical summarizes
The figure below illustrates the proposed architecture:
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/A%20Hybrid%20Neural%20Network-Latent%20Topic%20Model/f1.png" width=760>

#### Model Learning
1. Input SIFT decriptor, maximize the posterior distribution of class labels
2. Pre-train the neural network: by learning RBMs with the same structure in an unsupervised manner.
3. Pre-train the hierarchical topic Model: use the output of pre-trained NN as input to the HTM. The training is performed by Gibbs sampling as shown in below: <br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/A%20Hybrid%20Neural%20Network-Latent%20Topic%20Model/f2.png" width=340>
4. Joint optimization by gradient descent: Gradient descent is applied to update the parameters. The loss function can be expressed as follows:<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/A%20Hybrid%20Neural%20Network-Latent%20Topic%20Model/f3.png" width=340>
