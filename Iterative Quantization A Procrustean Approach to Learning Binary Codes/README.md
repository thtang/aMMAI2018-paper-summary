# Week 1: Iterative Quantization
Iterative Quantization: A Procrustean Approach to Learning Binary Codes <br>
*Yunchao Gong and S. Lazebnik. CVPR 2011*

## Background & Abstraction
Learning similarity-preserving binary codes for representing large-scale image collections has been widely discussed recently. There are three main constraints makes the binary code learning problem quite challenging: 
1. The codes should be short to deal with memory issue.
2. The codes should map images that are similar to binary strings with a low Hamming distance.
3. The algorithms should be very efficient.

Some algorithms have been proposed, for example, using PCA to reduce the dimensionality. However, the **information** contained in each PCA direction is different, so encoding each direction with **the same number** of bits is bound to produce poor preformance. 

## Goal 
Improve performance of binary coding

## Contribution 
