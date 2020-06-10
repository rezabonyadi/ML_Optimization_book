# Dimensionality reduction

### Introduction

Assume that you have a classification problem, an input dataset $X$, with $m$ instances \(rows\) and $n$ features \(columns\), and response $Y$. If $n$ is very large then it might lead to performance issues with some algorithms for classification. Hence, it is desirable to find a way to represent the same dataset, with all $m$ rows, with smaller number of features. This can be done in two ways: ignoring the responses \(supervised dimensionality reduction\) or taking into account $Y$ \(supervised\). Unsupervised dimensionality reduction finds a representation of $X$ with smaller number of features. This, however, may damage some structures in the data that are important for the classification task. Supervised dimensionality reduction finds a representation with smaller $n$, taking into account the classes $Y$.

### More details

This can be formulated in general as: let f\(., \theta\): R^p -&gt; R^n, and g\(., \omega\): R^n -&gt; R^p, p&lt; n, find \theta and \omega in a way that \|\|X-f\(g\(X, \omega\), \theta\)\|\| is minimized. For PCA, g\(X, \omega\) is XM, where M is a n by p matrix \(assuming X is m by n\) and g\(X, \theta\) is psodu-inverse of M \(which is p by n\).



\#\#TOCOMPLETE

#### 

