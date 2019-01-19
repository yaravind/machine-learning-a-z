## Linear Discriminant Analysis

LDA can be used for two-class or multi-class *classification* problems. LDA searches for the projection of a dataset which maximizes the **between class scatter to within class scatter** ratio of this projected dataset.

![Intuition](https://www.python-course.eu/images/Linear_Discriminant_Analysis_concept_illustration.png)

Assumptions

- Classes are well seperable
- Input variables follow Guassian (bell curve) distribution
- Remove outliers from data
- Each input variable of the same class has the same variance. It is almost always a good idea to standardize input data so that they have mean of zero and standard deviation of 1
- The mix of data in the training set is representative of the problem

## Reference

- [Intuition](https://www.python-course.eu/linear_discriminant_analysis.php)