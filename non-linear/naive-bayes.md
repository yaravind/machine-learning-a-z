# Naive-Bayes Algorithm

- It is called *Naive* because it makes a naive assumption that each feature is independent of other features which is not true in real life.
- It is a probablistic classifier based on well-known Bayes theorem with strong independence assumptions between the features
- Computationally faster, simple to implement and works well with high-dimensional datasets
- Can handle missing valyes well
- Adaptable since the model can be modified with new training data *without rebuilding the model*

## Spark

- Supports multinominal NB and Bernoulli NB (usefule if the feature vectors are Binary) implementations