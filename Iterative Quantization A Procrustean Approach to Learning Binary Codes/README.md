# Week1 summarization
Iterative Quantization: A Procrustean Approach to Learning Binary Codes[[1]](http://www.cs.unc.edu/~lazebnik/publications/cvpr11_small_code.pdf) <br>
*Yunchao Gong and S. Lazebnik. CVPR 2011*

## Goal 
Improve performance and efficiency of binary coding for large-scale image collections retrieval.

## Background & Abstraction
Learning similarity-preserving binary codes for representing large-scale image collections has been widely discussed recently. There are three main constraints makes the binary code learning problem quite challenging: 
1. The codes should be short to deal with memory issue.
2. The codes should map images that are similar to binary strings with a low Hamming distance.
3. The algorithms should be very efficient.

Some algorithms have been proposed, for example, using PCA to reduce the dimensionality. However, the **information** contained in each PCA direction is different, so encoding each direction with **the same number** of bits is bound to produce poor preformance. 

## Contribution 
1. Proposed approach **iterative quantization (ITQ)** outperforms the methods of [[2]](https://papers.nips.cc/paper/3749-locality-sensitive-binary-codes-from-shift-invariant-kernels), [[3]](http://www.ee.columbia.edu/ln/dvmm/publications/12/PAMI_SSHASH.pdf), [[4]](https://papers.nips.cc/paper/3383-spectral-hashing)
2. The method, **ITQ**, can be coupled with any projection on an orthogonal basis.

## Proposed method
The proposed method consists of two step:
1. Apply linear dimensionality reduction to the data (PCA here). The objective function are shown below:
+ original objective function
+ adaptive objective function
