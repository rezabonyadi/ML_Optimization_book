# Regularization

Let's assume that we are fitting a model $$M(X, \theta)$$ to the instances $$X$$, given labels $$Y$$, using an optimization algorithm and an evaluation metric, $$E(M(X, \theta), Y)$$, which provides a scalar describing how dissimilar is $$M(X, \theta)$$ to the corresponding $$Y$$.

$$
\min_{\theta} ~E(M(X, \theta), Y)
$$

Depending on the definition of $$E$$ and $$M$$, this problem might not have a unique solution. Hence, the optimization algorithm should be informed which solution is more acceptable so that it converges to what it supposed to. It is also possible that the optimizer perceives an "illusion" of better solutions, see \[@bonyadi2019optimal\] for details.

Here comes regularization. It provides another constraint, formulated into the objective function for convenience \(see section Lagrangian to see how is this possible\), to make the solution unique and regulate the illusions, as follows:

$$
min_{\theta} ~E(M(X, \theta), Y) + \alpha R(\theta)
$$

where $$R(\theta)$$is the regularization term and $$\alpha$$ is the regularization weight.

### Famous types

As the idea is a "simpler" model has a better chance to generalize better \(see Section \@ref\(sec:biasVariance\)\), the regularization term is defined in a way that it simplifies the model. Two of most frequently used regularization terms are called 

* $$L_1$$ \(aka LASSO\) defined by $$\||\theta||_1=\sum_i |\theta_i|$$
* $$L_2$$ \(special case of Tikhonov\), defined by $$||\theta||_2=\sum_i \theta_i^2$$
* $$L_0$$ regularization has also been investigated, which takes into account the minimization of the number of non-zero terms \(cardinality\), which becomes an NP-Hard problem. To resolve this, the l0 terms is approximated by a differentiable function. See this for l0 regularization: [http://ee.sharif.edu/~SLzero/](http://ee.sharif.edu/~SLzero/)



### More details

The regularization introduced in Eq. \@ref\(eq:optimizationregularized\) can be defined by a constrained optimization problem as follows:

\begin{equation} min\_{\theta} ~E\(M\(X, \theta\), Y\)+\alpha \epsilon s.t. R\(\theta\) = \epsilon \end{equation}

The Lagrangian of this problem is equivalent to the original definition of regularization in Eq. \@ref\(eq:optimizationregularized\). If $R\(\theta\)$ is the $L\_1$, this constraint limits the values of the parameters $\theta$ within a hyper cube, parameterized by $\epsilon$. If $L\_2$ is used, however, the parameter values are limited to a hyper-sphere, parameterized by $\epsilon$.

See \[wekipedia\]\([https://en.wikipedia.org/wiki/Regularization\_\(mathematics](https://en.wikipedia.org/wiki/Regularization_%28mathematics)\)\) for more information on this.

