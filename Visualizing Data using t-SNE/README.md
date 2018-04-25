# Week7 summarization
### Visualizing Data using t-SNE [[1]](http://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf)
*Laurens van der Maaten, Geoffrey Hinton; JMLR, 2008.*

## Background
1. Visualization of high-dimensional data is an important problem in many different domains
2. Dimensionality reduction methods convert the high-dimensional data set into two or three-dimensional data that can be displayed in a scatterplot. (aim to preserve as much of the significant structure of the high-dimensional data as possible in the low-dimensional map
3. Most of the techniques are not capable of retaining both the local and the global structure of the data in a single map.
## Contribution
1. t-SNE is capable of capturing much of the local structure of the high-dimensional data very well.

## Technical summarizes
#### Stochastic Neighbor Embedding
1. Converting the high-dimensional Euclidean distances between datapoints into conditional probabilities that represent similarities. The similarity of datapoint **x***j* to datapoint **x***i* is the conditional probability:<br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f1.png" width="220">
2. For the low-dimensional counterparts **y***i* and **y***j* of the high-dimensional datapoints **x***i* and **x***j*, model their similarity by <br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f2.png" width="220">
3. Find standard deviation σi of the Gaussian that is centered over each high-dimensional datapoint. SNE performs a binary search for the value of σi that produces a **P***i* with a fixed perplexity which is specified by the user.<br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f5.png" width="200"><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f6.png" width="200">


4. If the map points **y***i* and **y***j* correctly model the similarity between the high-dimensional datapoints **x***i* and **x***j*, the conditional probabilities **p***j*|*i* and **q***j*|*i* shold be equal. Therefore, SNE minimizes the sum of **KL divergences** over all datapoints using a gradient descent method.<br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f3.png" width="220"><br>Gradient computing:<br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f4.png" width="260">

#### t-Distributed Stochastic Neighbor Embedding
1. Modify the cost function to <br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f7.png" width="260"> <br>and that makes the similarity matrix to be symmetric.
2. The probability function to model the similarity in low or high dimension (with constraint to deal with outlier **x***i*) are shown below: <br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f8.png" width="220"><br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f9.png" width="220">
3. Optimize the cost function by gradient descent. <br>Gradient coomputing: <img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f10.png" width="220">
4. Since **crowding problem** exists in symmetric SNE, t-SNE use **Student t-distribution** with one degree of freedom, which has much heavier tails than a Gaussian to convert distances into probabilities, in low-dimensional map. The joint probabilities **q***ij* are defined as <img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f11.png" width="220">
5. The gradient become<br><img src="https://github.com/thtang/aMMAI2018-paper-summary/blob/master/Visualizing%20Data%20using%20t-SNE/f12.png" width="220">
