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
1. Converting the high-dimensional Euclidean distances between datapoints into conditional probabilities that represent similarities. 
