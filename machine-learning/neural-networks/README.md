# Neural networks

### Introduction

Great question. Classification and regression are done by optimizing a “model” \(a parametrized mathematical equation\) which is expected to describe the data. A linear model is the simplest one while a deep network represents a highly flexible model for which the “Weights” are optimized by an optimization method \(e.g., gradient descent\) on the given data.

If the number of data points is equal to or larger than the number of variables then the linear model has a unique global optimum, which is the only local optimum \(so, basically one optimum\). Hence, simple gradient descent can solve it to optimality \(i.e., find the best linear model\). For a highly flexible model like deep neural networks, the less data you have, the more local optima would appear in that highly flexible equation, which means there is a larger chance that the found local optimum by the optimization algorithm is far from the global optima. Hence, the more data you have the better until the global optimum is the only local optimum. Note, however, that if your network does not have many weights then you would not need many training instances too \(as a rule of thumb\).

{% embed url="http://playground.tensorflow.org/" %}



