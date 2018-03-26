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

## Technical summarizes
*The algorithm :<br>*
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Online%20Dictionary%20Learning%20for%20Sparse%20Coding/a1.png" width="320">
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Online%20Dictionary%20Learning%20for%20Sparse%20Coding/a2.png" width="320"><br>
The sparse coding problem with fixed dictionary is an **l1-regularized linear least-squares** problem. From the above algorithm, we can find out that [**LARS-Lasso algorithm**]("https://watermark.silverchair.com/200389.pdf?token=AQECAHi208BE49Ooan9kkhW_Ercy7Dm3ZL_9Cf3qfKAc485ysgAAAdEwggHNBgkqhkiG9w0BBwagggG-MIIBugIBADCCAbMGCSqGSIb3DQEHATAeBglghkgBZQMEAS4wEQQMqztjZbB5g2-lsUhcAgEQgIIBhPlHvs4aJUTzczfZ43HQwvSjUqYC6D6z_KGBc-O_L-H5Hz6vObISaGSTp3DBwWAjuFFGbRdklJCfCEVKMjGAy25b05wgVOs9ys5s5cBNjY5NzLdQBxBdub0BMu27dLf9qROSO19CbRqmn57-pe5BGN5skgVA2etutS0zkWC2ErUnzsqUeAUM7UWA3fBbtmID-XTFbwWpDirNrIEc4SxKhVWOUl0f9vB-Ic1XcSBb8QasFxv6X6oKwGvAvZHGoji7dNFiGgVUk2bcoqnM7QIWLK7VIj5z7MljSu9g6xdfjumFyD4fEk5-0STLvjkBSLYHkKAevBjlCN_9c5mDlfQRq--oHpnlyl5if8EWeOl2ibvL-AuSvj3hf5TDUyTGC-yOPxyepPvaxWIsk9-mIKRSmrqtBnHdYbQSKTqN9dowxM15LCSChSjD2O8l5dK-OqLzw9hwe_GtCjFed0lW7w6E7Dsp8SubZp1IX2yOKj9NvVjCQgS_s2LLn49fMxxFdJE34omRGts") is used to solve it. For parameter-free property of the above algorithm, **block-coordinate descent** with warm restarts is used.
## Experiment and result
**Compares proposed method with stochastic gradient descent**
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Online%20Dictionary%20Learning%20for%20Sparse%20Coding/f1.png" >
The above figure shows the advantage of a proposed method, but stochastic gradient descent somehow performs competitively.

The paper also demonstrates that the proposed method can indeed be applied to a realistic image processing task on large image, e.g., **Impainting**. Remove the text from the damaged 12-Megapixel image as shown in figure below.
<img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Online%20Dictionary%20Learning%20for%20Sparse%20Coding/f2.png" width="380">

## Reference
[1] Online Dictionary Learning for Sparse Coding <br>
[2] A new approach to variable selection in least squares problems
