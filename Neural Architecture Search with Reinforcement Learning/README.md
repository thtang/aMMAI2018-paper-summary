# Week13 summarization
### Neural Architecture Search with Reinforcement Learning [[1]](https://arxiv.org/pdf/1611.01578.pdf)
*Barret Zoph, Quoc V. Le, ICLR 2017*

## Goal
Design the neural networks architecture automatically.

## Background
1. Neural networks are hard to design. Beside, hyperparameter optimization is an important research topic in machine learning.
2. Previous works search models from a fixed-length space. Thus, those methods often work better with good initial model.
3. Some the other search-based methods are slow and require many heuristics to work well.

## Contribution
1. Leverage RNN to generate the model descroptions of NN.
2. The proposed method composes a noval recurrent cell that outperform LSTM cell.
3. The auto-built models reach comparable/state-of-the-art performances on CIFAR-10 and Penn Treebank dataset, respectively.


## Technical summarizes
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Neural%20Architecture%20Search%20with%20Reinforcement%20Learning/images/f1.png" width=420>
The proposed framework is shown in above figure. The network searching procedure follows below steps:

1. A RNN (**controller**) is used to generate variable-length string to describe structure and connectivity of a neural network (**child network**).
2. The child network would be trained with real data and output validation accuracy as reward signal for **policy gradient**.
3. Update the controller.



## Experiments
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Neural%20Architecture%20Search%20with%20Reinforcement%20Learning/images/t1.png" width=620>
800 GPUs are used for network searching. From the above table, comparable results on CIFAR-10 are reported.
