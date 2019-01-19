# machine-learning-a-z
Notebooks for [Machine Learning A-Z](https://www.youtube.com/playlist?list=PLclhPfG31KRExnNovDGE-ipPpKp9nRe2V)

Linear Models

- [Linear Regression]
- [Gradient Descent Algorithm](./gradient-descent.md)
- [Logistic Regression](./logistic-regression.md)
- [Linear Discriminant Analysis](./lda.md)
- [Batch vs Iteration vs Epoch](./batch-iteration-epoch.md)

Non-linear Models

- TBD

>Use StandardScaler for normally distributed data, otherwise use MinMaxScaler

Two main classes of ML algorithms

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
- Unsupervised
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

**The GOAL of good ML model is to generalize well from the training data to any data from the problem domain.**

**A fit referes to how well you approximate a target function**

## Formulae

Mean Squared Error

![Mean Squared Error](https://spin.atomicobject.com/wp-content/uploads/linear_regression_error1.png)

Partial Derivate for *m* and *b* (Used in Gradient Descent algorithm)

![Partial Derivative](https://spin.atomicobject.com/wp-content/uploads/linear_regression_gradient1.png)
