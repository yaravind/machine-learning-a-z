# machine-learning-a-z

Notebooks for [Machine Learning A-Z](https://www.youtube.com/playlist?list=PLclhPfG31KRExnNovDGE-ipPpKp9nRe2V)

## Linear Models

A linear model is a **sum of weighted variables** that predicts a target output value given an input data instance.

- [Linear Regression]
- [Gradient Descent Algorithm](./linear/gradient-descent.md)
- [Logistic Regression](./linear/logistic-regression.md)
- [Linear Discriminant Analysis](./linear/lda.md)

## Non-linear Models

- [Decision Trees](./non-linear/decision-tree.md)
- [Naive Bayes](./non-linear/naive-bayes.md)
- [K-Nearest Neighbors](./non-linear/knn.md)
- [Support Vector Machines](./non-linear/svm.md)

## Others

- [Ensemble Learning](./ensemble-learning.md)
- [Batch vs Iteration vs Epoch](./batch-iteration-epoch.md)

>Use StandardScaler for normally distributed data, otherwise use MinMaxScaler
> techniques like regularization, feature scaling, and cross-validation are used to avoid common pitfalls like under- and overfitting

## Two main classes of ML algorithms

Parametric

> A learning model that summarizes data with a set of parameters of fixed size (independent of the number of training examples) is called a parametric model. No matter how much data you throw at a parametric model, it won’t change its mind
about how many parameters it needs. — Artificial Intelligence: A Modern Approach, page 737

Nonparametric

>Nonparametric methods are good when you have a lot of data and no prior knowledge, and when you don’t want to worry too much about choosing just the right features. — Artificial Intelligence: A Modern Approach, page 757

Comparison  | Parametric | Nonparametric
----------  | ----------- | ---------------
Benefits    | easier to understand | capable of fitting to a large number of functional forms
Benefits    | easier to interpret results | no assumptions or weak assumptions about underlying function
Benefits    | faster to learn from data | result in higher performance models for prediction
Benefits    | can work with less training data | /
Benefits    | can work well even if the fit to the data isn't perfect |  /
Limitations | by chosing a functional form these are highly constrained to the specific form | require more traing data to estimate the function
Limitations | suited for simple problems | slower to train as often they have more parameters to train
Limitations | in practice, unlikely to match the underlying mapping function | risk to overfit an harder to explain predictions
Examples | Linear Regression, LDA, Perceptron | Decision Trees, Naive Bayes, VM, Neural Networks

Another way to group ML algorithms is **by the way they learn**

- Supervised
  - classification
    - binary classification: only one target value (transaction fraud or not)
    - multi-class: target value is one of many descrete values
    - multi-label: multiple target values (Tagging webpage based on their content)
  - regression
- Unsupervised
  - used to explore and understand the strucutre and patterns in data
- Semi-Supervised

## Bias and Variance

- All *learning* error can be broken down into bias or variance error
- *Bias* and *Variance* provide the tools to understand the behavior of ML algorithms in the pursuit of predictive performance. Increasing the bias will decrease the variance. Increasing the variance will decrease the bias.
- The *prediction* error for any ML algorithm can be broken down into 3 parts:
    1. Bias error
    2. Variance error
    3. Irreducible error

## Induction and Deduction

Induction refers to learning general concepts from specific examples. Deduction seeks to learn specific concepts from general rules.

## High dimensional data

We call data is high-dimensional if the number of features is greater than the number of observations or it could mean that you suspect there are noisy features that contain little information, or anything in between.

> multiclass classification vs multilabel classification (where multiple labels are to be predicted for each instance. For more on Spark-based implementation for the multilabel classification, interested readers should refer to [Spark docs](https://spark.apache.org/docs/latest/mllib-evaluation-metrics.html#multilabel-classification.)

## Data Preprocessig

- Cleaning
  - Dealing with missing values
  - Dealing with erroneous data
  - Dealing with outliers
- Transformation
  - Changing data types (discretization)
  - Changing range of data values (normalization)
  - Adding variables
- Reduction
  - Feature selection
  - Sampling

## Formulae

Mean Squared Error

![Mean Squared Error](https://spin.atomicobject.com/wp-content/uploads/linear_regression_error1.png)

Partial Derivate for *m* and *b* (Used in Gradient Descent algorithm)
![Partial Derivative](https://spin.atomicobject.com/wp-content/uploads/linear_regression_gradient1.png)

## NLP

- [NLP Definitive Guide](https://monkeylearn.com/blog/definitive-guide-natural-language-processing/)