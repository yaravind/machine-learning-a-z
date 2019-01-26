# Naive-Bayes (NB) Algorithm

- It is called *Naive* because it makes a naive assumption that each feature is independent of other features which is not true in real life.
- It is a probablistic classifier based on well-known Bayes theorem with strong independence assumptions between the features
- Computationally faster, simple to implement and works well with high-dimensional datasets
- Can handle missing valyes well
- Adaptable since the model can be modified with new training data *without rebuilding the model*
- The representation for NB is probabilities. A list of probabilities is stored to file for a learned model. These include
  - Class probabilities: the probabilities of each class in the training set
  - Conditional probabilities: the conditional probabilities of each input value given each class value
- Basic NB assumes *categorical* data. The adaptation of NB for *real-valued input* data is called Gaussian NB

## Spark

- Supports multinominal NB and Bernoulli NB (usefule if the feature vectors are Binary) implementations