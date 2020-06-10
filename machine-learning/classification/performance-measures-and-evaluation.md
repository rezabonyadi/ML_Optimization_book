# Performance measures and evaluation

[https://medium.com/@wilamelima/metrics-to-measure-machine-learning-model-performance-e8c963665476](https://medium.com/@wilamelima/metrics-to-measure-machine-learning-model-performance-e8c963665476)

Consider we are solving a binary \(2-class\) classification problem using a classification algorithm. Let's assume there are 100 items of class 1 and 200 of the class 0 in our training set. The classifier uses this data set to learn the patter of the data and provide a general rule to classify the instances. After training, it can classify 75 items of the class 0 and 190 of the class 1 correctly. Now, the question is, how well the classifier is doing its job? One simple way is to calculate the error percentage: $100\frac{75+190}{100+200}=88.3$ percent. But is this number a good indicative of how well the classifier is performing?

#### Signal detection

Signal detection claims that the error percentage is not an accurate measure of performance as it ignores the frequency of the items. For example, in the example above, the number of items in class 0 is twice as much as the the number of items in the class 1. This is usually the case in real-world data sets, i.e., the number of items in classes is imbalance \(the number of unhealthy subjects is much smaller than the number of healthy ones\). This poses lots of complications to the evaluation of classification methods. For example, assume that the number of items in one class is 100 times larger than the number of items in the other. Mis-classification of items from the smaller class leads to more "catastrophic" decisions as the more rare events are usually the most valuable ones which need to be detected correctly.

Traditionally, it is assumed that the items in class 1 are the ones we want to recognize \(e.g., unhealthy subjects\) and items in class 0 are "normal" items. In reality, the frequency of items in class 1 is usually much smaller than the items in class 0. Note that, algebraically, the class labels do not make any difference to the problem and its solution. Here, however, for the sake of definitions, we consider class 1 as positive recognition of items.

Signal detection measures four metrics to quantify performance: False positive, true positive, false negative, and true negative.

* _**False positive**_ \(aka false alarm\) is the number of responses which the classifier recognized as class 1 while they actually belong to class 0 \(i.e., falsely recognized as positive\). This is very important to be high when the number of instances in the classes is not balance. For example, if a classifier which is used for diagnosing an illness has a high false positive, it is likely to diagnose a healthy person as ill. Another example would be using a classifier to either invest or not to invest money on a business. High false positive would lead to loss of money.
* _**True positive**_ \(aka hit\) is the number of responses which the classifier recognized as 1 and they actually belong to class 1. We desire this to be as high as possible. This, however, might not be as important as it sounds. For example, in the investment example, one would prefer to deal with a low false positive and not to loose money than always invest correctly. In fact, a less frequent correct investment \(low true positive\) is ok, but not loosing money \(low false positive\) is very important.
* _**False negative**_ \(aka miss\) is the number of responses which the classifier recognized as 0 and they actually belong to class 1. This is particularly important in the illness diagnosis example. In fact, it is preferred to diagnose someone with a terminal illness \(high false positive\) and prescribe some more tests than missing if the person has a terminal illness and lead to their death. 
* _**True negative**_ \(aka \) is the number of responses which the classifier recognized as 0 and they actually belong to class 0. 

These four measures provide a better tool to evaluate the performance of the classifier. The importance of these factors, however, is problem dependent, as described by examples.

See [this page](http://ai-a2z.blogspot.com/2020/05/using-false-predictions-to-your-benefit.html) for more information.

#### Receiver operating characteristic \(ROC\) and Area under the curve \(AUC\)

\#\#TOCOMPLETE

#### Confusion matrix

\#\#TOCOMPLETE

#### 



#### Benchmarking

\#\#TOCOMPLETE

#### 

[https://github.com/EpistasisLab/penn-ml-benchmarks](https://github.com/EpistasisLab/penn-ml-benchmarks) [https://www.openml.org/home](https://www.openml.org/home)

#### Stratified sampling

\#\#TOCOMPLETE

#### 

#### Cross validation and random permutation

\#\#TOCOMPLETE

#### 

#### Imbalance data sets

\#\#TOCOMPLETE

#### 

_\*\*\*\*_

