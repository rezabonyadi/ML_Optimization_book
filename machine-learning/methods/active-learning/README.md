# Active learning

Active learning concerns machine learning paradigms in which the learner asks questions, from an Oracle, to improve its understanding of the topic it is learning, also known as one of the first attempts to build a “curious machine”. Essentially the learner plays an active role in picking the best next instance to learn from. See this: [http://burrsettles.com/pub/settles.activelearning.pdf](http://burrsettles.com/pub/settles.activelearning.pdf)

It can be used potentially in **interactive data annotation**: We usually have a small set of instances with labels and the rest are not labeled. This approach would enable labeling only if needed \(i.e., the learner wants the instance to be labeled\). We have been facing this issue in our image recognition datasets as finding labeled images in the area of mining is not easy.

