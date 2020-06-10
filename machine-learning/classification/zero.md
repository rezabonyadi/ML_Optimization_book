# Zero/one loss

### What that is

Assuming a binary classification problem \(two classes\) with a linear model, the objective is to find a hyperplane that "optimally" discriminates between the classes. To do so, we need an evaluation procedure which measures a "wrongness" score for any given hyperplane \(called the _loss function_\). Then, an optimization algorithm searches over all possible hyperplanes to find the one which minimizes the loss function \(see figure below\). 

![The objective is to find a line/hyperplane that separates the instances optimally. The search continues until a suitable hyperplane, evaluated by the loss function, is found. The final line found in this example classifies all instances correctly except one.](../../.gitbook/assets/finding_line_n.gif)

One simple loss function would be to count the number of instances that are not in the "correct" side of the hyperplane, called the _0/1 loss function_. The outcome of this minimization is a hyperplane which has a minimum 0/1 loss value, i.e., the number of instances that are in the wrong side of the hyperplane is minimized.

{% hint style="info" %}
One should note that there might be many hyperplanes which have the same 0/1 loss value, which means the solutions to the 0/1 loss function is not unique. In Fig. above, for example, the 0/1 loss value is the same for the green line and the orange line.
{% endhint %}

### When to use

The method is not sensitive to outliers \(see below\), hence useful when there are lots of outliers.

![](../../.gitbook/assets/image%20%2810%29.png)

### New advances

* The 0/1 loss function in its original form does not take into account the _importance_ of the instances from different classes \(all classes are assumed to be equally important\). See [this article ](https://arxiv.org/pdf/1804.09891.pdf)on how to address this. 
* This process does not provide a unique line. This is solved by selecting the line \(hyperplane\) which has the maximum distance from the instances of both classes \(see [this](https://arxiv.org/pdf/1804.09891.pdf)\), called maximum margin hyperplane, the one which has the maximum distance from each class is preferred. 
* Other improvements in included addition of $L\_1$ and $L\_2$ regularization, that enables the usage of coefficients for estimation of variable importance.
* Find a set of methods in [this article](http://proceedings.mlr.press/v28/nguyen13a.pdf).

{% hint style="success" %}
Are loss functions are the same? Read [here](http://web.mit.edu/lrosasco/www/publications/loss.pdf).
{% endhint %}

### Pros and cons

_Pros_: The 0/1 loss function is unbiased and not sensitive to outliers as any outlier would only contribute 1 unit to the loss function if it is miss-classified.

![](../../.gitbook/assets/image%20%289%29.png)

_Cons_: The main issue with this idea \(optimal 0/1 binary classification, with or without maximum margin idea\) is that optimizing the 0/1 loss function in the formed mentioned before is not practical, i.e., it is NP-Complete. Hence, all algorithms which implement this idea are rather slow. The only practically fast implementation has been described in [here](https://arxiv.org/pdf/1804.09891.pdf), which uses evolutionary strategy for optimization. This has encouraged introduction to lots of new loss functions which approximate the 0/1 loss function while they are differentiable.

### Implementation

* Methods described in [this](http://proceedings.mlr.press/v28/nguyen13a.pdf) are in an algorithmic, step by step, format which makes implementation easier. 
* The Python, Java, and Matlab code for this [paper](https://arxiv.org/pdf/1804.09891.pdf) is available [here](https://github.com/rezabonyadi/LinearOEC).

### Useful links

{% embed url="https://github.com/rezabonyadi/LinearOEC" %}



