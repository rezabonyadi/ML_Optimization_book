# Bayes classifier

### What that is

For a classification task, Bayes classifier calculates how likely it is that a given instance belongs to each class. Intuitively, the probability that a given instance, $\vec x$, belongs to a class $c$ depends on two main components:

* _Prior_: How likely it is that any given instance belongs to the class $c$ in general. 
* _Likelihood_: If we know an instance from class $c$, how likely it is that instance looks like $\vec x$.

For any given instance, we calculate these two and multiply their values. The outcome is a measure \(not exact\) of the probability if that instance belongs to class $c$. The larger this value, the more likely it is that the instance belongs to the class $c$.

This approach is called the _Bayes optimal classifier_. The first component is easy to calculate given the history. We can simply count the number of instances in the class $c$ and divide that by the total number of training instances, which represents how likely it is that an instance come from that class. The second component is very difficult, if possible, to calculate if we assume that the attributes are not independent. The reason is each instance is a _mix_ of multiple attributes, some might be the same as what has been observed in the training set, some might not be. The comparison between these instances to calculate the _likelihood_ is difficult as all attributes need to be considered at the same time. If we assume independence between variables, however, that probability is calculated easily. This is called the _Naive Bayes_ classifier because the independence assumption is somewhat "naive". For a given instance $\vec x$, for each attribute, we calculate how likely it is that an instance from class $c$ has the same value as of $\vec x$ for that attribute, i.e., attributes are independent. We then multiply those probabilities which would be an estimate of the original likelihood with mixed variables.

See [wikipedia page](https://en.wikipedia.org/wiki/Naive_Bayes_classifier) and [this](https://www.geeksforgeeks.org/naive-bayes-classifiers/) for examples.

For discrete variables it is rather easy to calculate the probabilities based on the given instances. For continuous variables \(e.g., age, weight\), however, this probability needs to follow a distribution. Given the distribution, one can calculate the probabilities. The [wikipedia page](https://en.wikipedia.org/wiki/Naive_Bayes_classifier) provides very good description on this algorithm.

### Pros and cons

\[khasdk\]\(\#what-that-is\) 





**Pros**:

* It is easy and very fast to predict class of test data set. 
* When assumption of independence holds, a Naive Bayes classifier performs better compare to other models like logistic regression and you need less training data.
* It performs well in case of categorical input variables compared to numerical variable\(s\). For numerical variable, normal distribution is assumed \(bell curve, which is a strong assumption and might not be correct\).
* It works well with sparse data-sets.
* Organically handle multiple classes.
* They are generative and can be easily interpreted as discriminative
* Missed values can be easily dealt with
* If the value for a variable is missed completely, they would still work with simple tricks \(not the case for many classifiers\)

**Cons**:

* If categorical variable has a category \(in test data set\), which was not observed in training data set, then model will assign a 0 \(zero\) probability and will be unable to make a prediction. This is often known as “Zero Frequency”. To solve this, we can use the smoothing technique.
* Another limitation of Naive Bayes is the assumption of independent predictors. In real life, it is almost impossible that we get a set of predictors which are completely independent.
* For continuous variables, it is assumed that the variables follow a given distribution \(usually normal\) to be able to calculate the probability, which may not be accurate. 

### Implementation

* For implementation from scratch see [here](https://www.analyticsvidhya.com/blog/2017/09/naive-bayes-explained/). 
* In Python, [scikit-learn](https://scikit-learn.org/stable/modules/naive_bayes.html) can be used.



