# Logistic regression

### Introduction

Logistic regression seeks a hyperplane which best discriminates two classes. The hyperplane is evaluated by a loss function which is a smooth \(differentiable\) estimation of the function used in the 0/1 loss function, hence, can be optimized effectively by a gradient descent. While there might be many different choices for such function, logistic regression uses the logarithm sigmoid function that looks like Fig. \@ref\(fig:logsig\).

More details on this algorithm can be found in [Stanford University Tutorial on Supervised Learning](http://ufldl.stanford.edu/tutorial/)

A derivative of Logistic Regression is the General Linear Model \(GLM\). ???



```text
### Interpretability

* The coefficients of the hyperplane found by the logistic regression **cannot** be interpreted directly as indicator for variable importance. The reason is that the variables ranges might be inherently different, meaning that some coefficients need to be larger to compensate for larger values. For example, if the values of one variable is in the range of 1000 and the other is in the range of 0.1, it is expected that the coefficients related to the first variable to be larger. This, however, does not show that the first variable is more important than the second.
* If the value of variables are standardized (see Section \@ref(sec:preprocessing)), however, the coefficients can be used as indicators of importance. The smaller the absolute value of a coefficient is, the less important that variable is. To imagine this, think of a variable that is not important at all (see Fig. \@ref(fig:variableImport)), i.e., from the perspective of that variable, the instances from both groups are the same. We expect the discriminatory hyperplane to have a small or zero coefficient value for that variable. 

```

```text
```{r variableImport, echo = FALSE, out.width = '49%', fig.show = "hold", fig.cap = '????.'}
knitr::include_graphics(c('images/classification/v_importance_logistic_func_1.PNG', 'images/classification/v_importance_logistic_func_2.PNG'))
```

#### Pros and cons

* Pros
  * It is easy to implement
  * Can be effectively solved by second order optimization methods
  * It supports sparse representation of data 
* Cons
  * Might not provide the most generalizable line

#### Implementation

* **Implementation from scratch**: see [Stanford University Tutorial on Supervised Learning](http://ufldl.stanford.edu/tutorial/). 
* **In Python**: the [Scipy](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.logistic.html) library and the [Sikit-Learn](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html) library both have implementation of this.

