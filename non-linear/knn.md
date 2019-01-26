# K-Nearest Neighbot (KNN)

- Can be used for classification or regression
- Lazy algorithm: KNN does not use the training data points to do any *generalization*. In other words there is no explicit *training phase*. So this means that KNN requires all (or most) training data during the prediction
- Predictions are made for a new data point by searching through the entire training set for the *k* most similar instances (the neighbors) and summarizing the output variable for those *k* instances.
  - For finding neighbors you can use
    - Eucledean distance
    - Manhattan distance
  - For regression, the summarization might be the *mean or median of k neighbors*
  - For classification, this might be *mode or the most common class*

> Learning Vector Quantization is an extension of KNN for classification

## Pseudocode for the algorithm

1. Load the data
2. Initialise the value of k
3. For getting the predicted class, iterate from 1 to total number of training data points
  3.1. Calculate the distance between test data and each row of training data. Here we will use Euclidean distance as our distance metric since it’s the most popular method. The other metrics that can be used are Chebyshev, cosine, etc.
  3.2. Sort the calculated distances in ascending order based on distance values
  3.3. Get top k rows from the sorted array
  3.4. Get the most frequent class of these rows
  3.5. Return the predicted class

## Reference

- [Source of pseudocode](https://www.analyticsvidhya.com/blog/2018/03/introduction-k-neighbours-algorithm-clustering/)
- [KD Tree usecases](https://www.quora.com/What-is-a-kd-tree-and-what-is-it-used-for)