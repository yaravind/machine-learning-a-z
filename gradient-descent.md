Disclaimer: Copied from [ds  repo here](https://github.com/vangj/ds).

# Gradient descent

Gradient descent is an optimization algorithm to find the minimum of some function. Typically, in machine learning, the function is a loss function, which essentially captures the difference between the true and predicted values. Gradient descent has many applications in machine learning and may be applied to (or is the heart and soul of) many machine learning approaches such as find weights for

- regression,
- support vector machines, and
- deep learning (artificial neural networks).

This notebook aims to show the mechanics of gradient descent in an easy way.

## Simple linear regression
Let's say we have a simple linear regression.

```
y = b + mx
```
where,

- `b` is the y-intercept (or bias),
- `m` is the coefficient (or slope),
- `x` is the an independent variable value, and
- `y` is the predicted, dependent variable value.

Now, we want to estimate `m`. There are many ways to estimate `m`, however, we want to use gradient descent to do so (we will not go into the other ways to estimate `m`). The first thing we have to do is to be able to formulate a loss function. Let's introduce some convenience notation. Assume y&#770;  is what the model predicts as follows.

`y&#770; = f(x) = b + mx`

Note that ![hat](http://latex.codecogs.com/svg.latex?%5Chat%7B%5Cmathbf%7By%7D%7D)  is just an approximation of the true value `y`. We can define the loss function as follows.

L(![hat](http://latex.codecogs.com/svg.latex?%5Chat%7B%5Cmathbf%7By%7D%7D) , y) = (y - ![hat](http://latex.codecogs.com/svg.latex?%5Chat%7B%5Cmathbf%7By%7D%7D) )^2 = (y - (b + mx))^2

The loss function essentially measures the error of the model; the difference in what it predicts ![hat](http://latex.codecogs.com/svg.latex?%5Chat%7B%5Cmathbf%7By%7D%7D)  and the true value `y`. Note that we square the difference between `y` and ![hat](http://latex.codecogs.com/svg.latex?%5Chat%7B%5Cmathbf%7By%7D%7D)  as a convenience to get rid of the influence of negative differences. This loss function tells us how much error there is in each of our prediction given our model (the model includes the linear relationship and weight). Since typically we are making several predictions, we want an overall estimation of the error.

L(![hat](http://latex.codecogs.com/svg.latex?%5Chat%7B%5Cmathbf%7By%7D%7D) , Y) = 1/N Σ{(y - ![hat](http://latex.codecogs.com/svg.latex?%5Chat%7B%5Cmathbf%7By%7D%7D)^2} = 1/N Σ(y - (b + mx))^2

But how does this loss function really guides us to learn or estimate `m`? The best way to understand how the loss function guides us in estimating or learning the weight `m` is visually. The loss function, in this case, is convex (U-shaped). Notice that the functional form of the loss function is just a squared function not unlike the following.

`y = f(x) = x^2`

If we are asked to find the minimum of such a function, we already know that the lowest point for `y = x^2` is `y = 0`, and substituting `y = 0` into the equation, `x = 0` is the input for which we find the minimum for the function. Another way would be to take the derivative of `f(x)`, `f'(x) = 2x`, and find the value `x` for which `f'(x) = 0`.

However, our situation is slightly different because we need to find `b` and `m` to minimize the loss function. The simplest way to find the minimum of the loss function would be to exhaustively iterate through every combination of `b` and `m` and see which pair gives us the minimum value. But such approach is computationally expensive. A smart way would be to take the first order partial derivatives of `L` with respect to `b` and `m`, and search for values that will minimize simultaneously the partial derivatives.

1. *`dL/db`*` = 2/N * Σ-(y - (b + mx))`
2. *`dL/db`*` = 2/N * Σ-x(y - (b + mx))`

Remember that the first order derivative gives us the slope of the tanget line to a point on the curve.

At this point, the gradient descent algorithm comes into play to help us by using those slopes to move towards the minimum. We already have the training data composed of `N` pairs of  `(y, x)`, but we need to find a pair `b` and `m` such that when plugged into the partial derivative functions will minimize the functions. The algorithm for the gradient descent algorithm is as follows.

- given
    - `(X, Y)` data of  `N` observations,
    - `b` initial guess,
    - `m` initial guess, and
    - `α` learning rate
- repeat until convergence
    - `∇b = 0`
    - `∇m = 0`
        - for each `(x, y)` in `(X, Y)`
            - `∇b = ∇b - 2/N * (y - (b + mx))`
            - `∇m = ∇m - 2/N * x(y - (b + mx))`
        - `b = b - α * ∇b`
        - `m = m - α * ∇m`
        
        
        x-bar = x&#772; or x&#x0304; (hex)
        
        p-hat = x&#770; or x&#x0302; (hex)
        
        View Results
        x-bar = x̄ or x̄ (hex)
        
        p-hat = p̂ or p̂ (hex)
