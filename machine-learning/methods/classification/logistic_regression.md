# Logistic regression

### What that is

Logistic regression seeks a hyperplane which best discriminates two classes. The hyperplane is evaluated by a loss function which is a smooth \(differentiable\) estimation of the function used in the 0/1 loss function, hence, can be optimized effectively by a gradient descent. While there might be many different choices for such function, logistic regression uses the logarithm sigmoid function that looks like below.

![](../../../.gitbook/assets/image%20%2811%29.png)

More details on this algorithm can be found in [Stanford University Tutorial on Supervised Learning](http://ufldl.stanford.edu/tutorial/)

A derivative of Logistic Regression is the General Linear Model \(GLM\). ???

### Pros and cons

* Pros
  * It is easy to implement
  * Can be effectively solved by second order optimization methods
  * It supports sparse representation of data 
* Cons
  * Might not provide the most generalizable line

### Implementation

* **Implementation from scratch**: see [Stanford University Tutorial on Supervised Learning](http://ufldl.stanford.edu/tutorial/). 
* **In Python**: the [Scipy](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.logistic.html) library and the [Sikit-Learn](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html) library both have implementation of this.



### Useful links

{% embed url="http://ufldl.stanford.edu/tutorial/" %}

{% embed url="https://scikit-learn.org/stable/modules/generated/sklearn.linear\_model.LogisticRegression.html" %}

{% embed url="https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.logistic.html" %}





