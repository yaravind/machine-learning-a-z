# Classification and Regression Trees (aka Decision Trees)

- CART algorithm is used for *classification* or *regression* predictive modeling problems. It provides a foundation for other algorithms like bagged decision trees, random forest and boosted decision trees.
    - For regression predictive modeling problems the cost function that is minimized to choose the split points is the *sum of squared error across all training samples that fall within a rectangle*
    - For classification the *Gini cost function* is used which provides how pure the leaf nodes are i.e. how mixed the training data assigned to each node is
- The model is represented as a binary tree. Each node represents a *single input variable (x)* and split point on that variable. The *leaf nodes of the tree contain an output variable (y) which is used to make prediction*.
- It doesn't require any special data preparation other than good representation of the problem.
- The final tree is stored to a file as a set of rules.

## Stopping criterion and Pruning

**Stopping criteria define how much a tree learns and pruning can be used to improve generalization on a learned tree.**

The stopping criterion strongly influences the performance of the tree. The splitting procedure needs to know when to stop splitting as it works its way down the tree with training data. The most common stopping procedure is to use a *minimum count on the number of training instances assigned to each node*.

We can use pruning after learning the tree to further lift performance. The complexity of a decision tree is defined as *the number of splits in the tree.* Simpler trees are preferred as they are easy to understand and less likely to overfit.