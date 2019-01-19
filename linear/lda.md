## Linear Discriminant Analysis

LDA can be used for two-class or multi-class *classification* problems. LDA searches for the projection of a dataset which **maximizes the between class scatter to within class scatter ratio** of this projected dataset.

![Intuition](https://www.python-course.eu/images/Linear_Discriminant_Analysis_concept_illustration.png)

### Illustration

![LD1 vs LD2](https://raw.githubusercontent.com/eigenfoo/eigenfoo.xyz/master/assets/images/lda-pic.png)

A couple of points to make:

- LD1 and LD2 are among the projections that LDA would consider. In reality, LDA would consider all possible projections, not just those along the x and y axes.
- LD1 is the one that LDA would actually come up with: this projection gives the best “separation” of the two classes.
- LD2 is a horrible projection by this metric: both classes get horribly overlapped… (this actually relates to PCA, but more on that later)

>Besides from classification also most commonly used as dimensionality reduction technique in the pre-processing step for pattern-classification and machine learning applications

Assumptions

- Classes are well seperable
- Input variables follow Guassian (bell curve) distribution
- Remove outliers from data
- Each input variable of the same class has the same variance. It is almost always a good idea to standardize input data so that they have mean of zero and standard deviation of 1
- The mix of data in the training set is representative of the problem

## Reference

- [Intuition](https://www.python-course.eu/linear_discriminant_analysis.php)
- [Applications of LDA](https://people.revoledu.com/kardi/tutorial/LDA/Applications.html)
- [Illustration](https://eigenfoo.xyz/lda/)