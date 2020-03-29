# Important considerations in machine learning

### The bias-variance debate  <a id="sec:biasVariance"></a>

Assume there is a set of given instances, $$X$$ \(m rows and n columns\), and we are asked to optimize a model $$M(X, \theta)$$ to estimate $$Y$$ \($$m$$ rows\) given some examples, i.e., supervised learning. Also, it is assumed that the underlying pattern of the data is not known \(note that, this is a very important assumption as if this is not true then any model except the one which formulates the pattern is irrelevant\). Another assumption is that the collected data may have some noise in it \(another important assumption\). If $M$ is a flexible formula \(which usually means it involves lots of parameters to complex formulations\) then it can fit to the given data-set very well. This, however, means that the model would formulate also the noise in the data, which would impose lots of fluctuations and non-linearities that are not really related to the pattern in the data but the noise in the observations. This leads to a model that has a low bias. However, as it is very flexible and formulates lots of fluctuations coming from random events \(noise\), it also offer a high variance. This high variance and low bias would lead to worsening the generalization ability of the model as it is not really formulating the pattern in the data but also the noise and unnecessary fluctuations.

Let's go a bit more detail. Let us call each instance $$x$$ and its corresponding desired output as $$y$$. In reality, $$y$$ is the outcome of a system working with inputs $$x$$, and some noise, $$y=f(x)+\epsilon$$, where $$f(.)$$ is not known and $$\epsilon$$ is noise which is also unknown. For example, if $$x$$ represents characteristics of people \(smoking habit, weight, genetics, etc.\) and $$y$$ is whether or not they would have a heart-attack after their 50s, then $$f(x)$$ is how body would respond to those characteristics and leads to a heart-attack or not, which is not really known. With modelling, we estimate this function $$f(x)$$, given some examples and some assumptions on the shape of $$f$$.

A model $$M$$ is responsible to estimate observed $$Y$$ as $$Y=f(X)+\epsilon=M(X, \hat{\theta})+e$$, where $$e$$ has $$m$$ rows and indicates the error from $$Y$$. If $$e$$ is small then $$M(X, \hat{\theta})$$ is an accurate estimation of $$Y$$, hence the model estimates not only $$f$$ but large amount of the noise $$\epsilon$$ in it. This takes place if the model $$M$$ is a complex, flexible, equation which is able to fit any complex behavior of $$Y$$ as function of $$X$$, including all fluctuations resulting from the noise. Hence, the outputs of the model will be similar to the values of $$Y$$ \(non-biased\), which includes noisy fluctuations, which leads to a high variance \(fluctuations usually lead to large variance\). If the model is not complex though, the gap between the output of the model and $$Y$$ might be large \(bias\), however, it would fit less to the noisy fluctuations in the $$Y$$ which leads to a smaller variance. That is why it is said a complex model has a large variance and small bias, and vice versa. Formal calculation of this trade off can be found in the [bias-variance tradeoff in wikipedia](https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff#Derivation).

### Regularization <a id="sec:regularization"></a>

Let's assume that we are fitting a model $$M(X, \theta)$$ to the instances $$X$$, given labels $$Y$$, using an optimization algorithm and an evaluation metric, $$E(M(X, \theta), Y)$$, which provides a scalar describing how dissimilar is $$M(X, \theta)$$ to the corresponding $$Y$$.

$$
\min_{\theta} ~E(M(X, \theta), Y)
$$

Depending on the definition of $$E$$ and $$M$$, this problem might not have a unique solution. Hence, the optimization algorithm should be informed which solution is more acceptable so that it converges to what it supposed to. It is also possible that the optimizer perceives an "illusion" of better solutions, see \[@bonyadi2019optimal\] for details.

Here comes regularization. It provides another constraint, formulated into the objective function for convenience \(see section Lagrangian to see how is this possible\), to make the solution unique and regulate the illusions, as follows:

\begin{equation} min\_{\theta} ~E\(M\(X, \theta\), Y\) + \alpha R\(\theta\) \(\#eq:optimizationregularized\) \end{equation}

where $R\(\theta\)$ is the regularization term and $\alpha$ is the regularization weight.

#### Famous types

As the idea is a "simpler" model has a better chance to generalize better \(see Section \@ref\(sec:biasVariance\)\), the regularization term is defined in a way that it simplifies the model. Two of most frequently used regularization terms are called $L\_1$ \(aka LASSO\) and $L\_2$ \(special case of Tikhonov\), defined by $\|\|\theta\|\|\_1=\sum\_i \|\theta\_i\|$ and $\|\|\theta\|\|\_2=\sum\_i \theta\_i^2$, respectively.

#### More details

The regularization introduced in Eq. \@ref\(eq:optimizationregularized\) can be defined by a constrained optimization problem as follows:

\begin{equation} min\_{\theta} ~E\(M\(X, \theta\), Y\)+\alpha \epsilon s.t. R\(\theta\) = \epsilon \end{equation}

The Lagrangian of this problem is equivalent to the original definition of regularization in Eq. \@ref\(eq:optimizationregularized\). If $R\(\theta\)$ is the $L\_1$, this constraint limits the values of the parameters $\theta$ within a hyper cube, parameterized by $\epsilon$. If $L\_2$ is used, however, the parameter values are limited to a hyper-sphere, parameterized by $\epsilon$.

See \[wekipedia\]\([https://en.wikipedia.org/wiki/Regularization\_\(mathematics](https://en.wikipedia.org/wiki/Regularization_%28mathematics)\)\) for more information on this.

Another useful regularization term is the $L\_0$ which counts the number of non-zero

### Raw data vs characterized data \(features\)

The data in its original form, raw form, represents what is measured. The measurements, however, are not always useful to learn from. For example, in a stock market signal, the actual close daily prices are not as important as the trend of those values. Hence, depending on the problem, some characteristics of the data might be more informative than the raw data itself. These characteristics are usually called features. Features basically represent important \(relevant to a given problem which uses that data for solution\) attributes of the problem. They are either designed by an expert \(i.e., feature engineering\) or optimized by an algorithm for a given model \(i.e., feature formation, popular in deep learning\). For example, assume that we want to characterize fruits. Some obvious features of fruits are their shapes \(e.g., being round, or egg-shaped, or long\), their tastes, and their smell. Features characterize attributes that distinguish different objects

For many problems, the features are already known. For example, we already know that a feed in a newspaper is considered interesting for a particular reader if the reader spends more time on it \(the spent time is a feature\). However, recognizing someone's face from an image is not easy to be defined by apparent features. This encourages methods like Deep Learning to not only learn the task but also find the best presentation for the problem, just from the raw data.

### Variable importance and insights considerations

Bootstrap aggregation 

Importance level

