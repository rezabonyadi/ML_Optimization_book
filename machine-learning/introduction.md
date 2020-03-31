# Introduction

Machine learning refers to a set of algorithms which make a machine \(with a computer as its brain\) to apparently learn. While learning in animals and human is not very well understood, in machines it is simply to find a generic rule, given a set of examples, which

Machine learning refers to a set of methodologies that make machines apparently "learning" to perform tasks. Although it is hard to define learning, it is related to progressive improvement in performing a task successfully. Intuitively there are two types of learning: self-learning \(unsupervised\) and learning from others \(supervised\).

Not fully observed, hence, there need to be assumptions as the solutions is not unique

### Supervised and unsupervised learning <a id="sec:supervisedvsunsupervised"></a>

In supervised learning the learner learns to accomplish a task with supervision, i.e., there is a set of instances that the learner learns from, or there is a system that provides feedback to the actions of the learner \(reinforcement\). Imagine for example you need a system to learn how to drive. For a human, we just hire an instructor and train the person and done. This is precisely the same for a machine, we provide instances or a feedback loop so that the machine can evaluate its performance and learns. Applications of supervised learning include self-driving cars, stock market prediction, object recognition, natural language processing, maintenance prediction, recommendation engines, weather forecast, and more.

In the unsupervised learning, the algorithm "figures out" the patterns in the instances, without any supervision. This is the more sophisticated while the most exciting use of machine learning. Customer segmentation, anomaly detection, product similarities, and many other applications require unsupervised learning.

A human or an animal learns from the environment by [re-structuring the connectivity of neurons in their brain](https://www.cam.ac.uk/research/features/lifelong-learning-and-the-plastic-brain). The phenomenon has not been well understood yet but, in the abstract level, it is just like branching a graph, with billions of nodes and connections, to work better with the learning task at hand. The aim is to provide a generic \(abstract\) representation of the problem and the solution in the brain that is accessible when needed. This, however, is slightly different for a machine. The problem needs to first be translated into a "mathematical space" \(coordinate systems, or simply numbers\),the instances \(samples of the learning task\) need to be presented by their basic components \(so-called features\) in a "vector space" \(numbers each with a particular meaning\).

### Supervised models <a id="sec:supervisedmodels"></a>

Let's assume a set of $$m$$ instances, $$X$$, with $$m$$ rows and $$n$$ columns \(each row is an instance and each column is a feature\) and their associated responses, $$Y$$, with $$m$$ rows, is given \(called the training data set\). A supervised model $$M(.,\theta)$$, $$\theta $$ being model parameters \(e.g., linear model\), provides a generic rule by which the response, $$y$$, is correctly estimated for any given instance, $$x$$ \($$1$$ row and $$n$$ columns\). The parameters $$\theta$$ are optimized by an optimizer for the model $M$ to best satisfy an _evaluation_ metric \(in some algorithms, this metric is called the _loss function_\) which evaluates how similar $$M(.,\theta)$$ is to actual $$y$$ for each $$x$$ and any given $$\theta$$.

Usually, the given instances \(training set\) do not represent all possible instances for a given problem. Therefore, any model, in any shape and form, that transforms $$X$$ to $$Y$$ and optimizes the evaluation measure is acceptable. This means defining "the best model", a model that not only separates the given instances but also all other unseen instances, is limited by the knowledge encoded in the training set. This incomplete knowledge about the data leads the designer to make some _assumptions_ on the model and the evaluation metric upon which different classifiers are formulated. For example, support vector machines in their original form assume that the discriminatory rule is represented by a line \(an assumption on the model, a linear model\) which has the maximum distance from the instances in each class \(an assumption on the evaluation metric\). The idea is that such a line is more empirically robust against potential uncertainties in unseen instances.

It is important to design the model carefully as it is responsible to represent the "pattern" in the data in the most generic \(low variance, see Section [bias\_variance](important-considerations.md#sec:biasVariance)\) and accurate \(low bias\) way. You may ask why not picking the most flexible mathematical equation in existence \(e.g., Taylor series\) and optimize its parameters to fit the given data? Flexible models \(e.g., deep networks\) may be able to fit the data well \(simply because they are flexible and can fit anything\), however, they might not be able to _generalize_ well, i.e., work well for unseen data. Sometimes the models come from specific knowledge about the problem, e.g., physics models.

### Why the hype?

See [this blog](http://ai-a2z.blogspot.com/2019/07/what-is-data-science.html) for more information on this topic.

Data science is the science of dealing with data to extract patterns, which, eventually, are used to present information about how future look like given the history. You have all seen the following picture as a mean of defining what is this data science:  


![](../.gitbook/assets/image%20%2810%29.png)

While the picture is quite telling, it has a lot of details to be clarified. Obviously, a data scientist requires Computer Science, Mathematics, and Domain knowledge. But each of these is, on their own, a large field of study. I personally believe that the more you know in these areas the better you will be in solving data science-related problems. However, "what do we need from each of these to get started" is a fair question.

Mathematics provide methodologies required to design solutions for problems. Methodologies like classification, clustering, statistical tests, and even neural networks have deep mathematical bases which enable their effectiveness in solving relevant problems. Computer science, however, provides techniques to implement these methodologies, ranging from programming languages, algorithmic design, complexity theory, software design and architecture, databases, cloud, among others. Clearly. skills from computer science and Mathematics provide tools to solve a problem, essentially what can we solve \(How to solve a problem\). However, they do not provide any information about what would worth solving, essentially what needs to be solved \(What to solve and why to solve it\). This information is provided by the domain knowledge \(or subject matter experts, SMEs\).

 Pure Mathematics is always well ahead of other sciences simply because it does not require much of infrastructure \(labs, equipment, etc.\). When it becomes apply, however, the issue of infrastructure comes into place. Most techniques used in data science are quite old. For example, the "State-of-the-art" convolutional neural network is nearly 25 years old \(see [this](https://www.researchgate.net/profile/Yann_Lecun/publication/2453996_Convolutional_Networks_for_Images_Speech_and_Time-Series/links/0deec519dfa2325502000000.pdf)\). Of course new advances have happened ever since, still, most used methods in data science are linear regression, support vector machines, among others. So, the question is, why data science has become so popular only recently if the knowledge already existed. Here are some reasons.  


* **Maturity of methods**: With the internet, the methods invented by mathematicians are shared more rapidly and publicized better, which makes them more accessible for whoever interested. In the meantime, many people simplify the methodologies for better understanding. 
* **Cheap data collection**: Sensors and electronic devices have become much more affordable than before. The cost of sensors is drastically reducing, in 2004 the average cost of sensors was $1.30 and in the year 2020, it is expected to come down to $0.38 \(see [this](https://www.ennomotive.com/industrial-iot-sensor-prices/)\). 

| ![Hard Drive Disc Comparison](https://2oqz471sa19h3vbwa53m33yj-wpengine.netdna-ssl.com/wp-content/uploads/2017/11/hard-disk-drive-viz.gif) |
| :--- |
| Size of hard-drives in years. See [this](https://www.visualcapitalist.com/visualizing-trillion-fold-increase-computing-power/) |

* **Cheap data storage**: The prices of storage hard drives per GB per year has dropped significantly. This enables easier data storage, hence, more data can be collected.

  | ![Hard Drive Cost per GB over time](https://www.backblaze.com/blog/wp-content/uploads/2017/07/chart-cost-per-gb-2017.jpg) |
  | :--- |
  | Cost of data storage per GB in time. See [this](https://www.backblaze.com/blog/hard-drive-cost-per-gigabyte/) |

* **Accessibility of data**: Internet is one of the most important factors that has increased accessibility to information significantly. This is required for a data scientist.
* **Much more compute power**: Convolutional neural networks were not publicized until 2012 when they were finally implemented on effective hardware, a massively parallelizable idea on GPU. Mainframes have been replaced by very accessible clusters and clouds. Processing power per CPU core has significantly increased \(see [Moore's law](https://en.wikipedia.org/wiki/Moore%27s_law)\). Apollo Guidance Computer which guided the space-craft to the moon had a CPU with 2 MhZ of clock and 4KB of RAM! Way way less power compared to our phones today. See [this](https://www.visualcapitalist.com/visualizing-trillion-fold-increase-computing-power/).

  
And we are still far behind the processing, memory, and storage power of the human brain:  


| ![Computer Brain Exascale](https://2oqz471sa19h3vbwa53m33yj-wpengine.netdna-ssl.com/wp-content/uploads/2017/11/computer-brain.jpeg) |
| :--- |
| How are we doing compared to nature? See [this](https://www.visualcapitalist.com/visualizing-trillion-fold-increase-computing-power/). |





