# machine-learning-a-z
Notebooks for https://www.youtube.com/playlist?list=PLBjazsVtMXXvl9miqmU2LTHNOnGGB7Yoa

Two main classes of ML algorithms

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