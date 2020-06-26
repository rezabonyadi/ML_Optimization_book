# Text summarization

### Introduction

Automatic text summarization is the task of producing a concise and fluent summary while preserving key information content and overall meaning

There are broadly two different approaches that are used for text summarization:

* Extractive Summarization
* Abstractive Summarization

### Extractive Summarization

The name gives away what this approach does. **We identify the important sentences or phrases from the original text and extract only those from the text.** Those extracted sentences would be our summary. The below diagram illustrates extractive summarization:

![text summarization](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/extractive1.jpg)

I recommend going through the below article for building an extractive text summarizer using the TextRank algorithm:

* [An Introduction to Text Summarization using the TextRank Algorithm \(with Python implementation\)](https://www.analyticsvidhya.com/blog/2018/11/introduction-text-summarization-textrank-python/)

### Abstractive Summarization

This is a very interesting approach. Here, **we generate new sentences from the original text.** This is in contrast to the extractive approach we saw earlier where we used only the sentences that were present. The sentences generated through abstractive summarization might not be present in the original text:

![abstractive summarization](https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/abstractive1.jpg)

### Implementation and libraries

**From scratch**

* For a simple example for Executive summarization see [this link](https://stackabuse.com/text-summarization-with-nltk-in-python/).
* For abstractive using deep learning see [here](https://www.analyticsvidhya.com/blog/2019/06/comprehensive-guide-text-summarization-using-deep-learning-python/) \(this is really great\).

**Packages**

* Use [Transformer ](https://huggingface.co/transformers/installation.html)package for a large set of different models \(easy to use\). NOTE, it needs pytourch to be installed too.
* See PEGASUS by Google here: 

### Read more

Read more here about details and implementation using deep learning:

{% embed url="https://www.analyticsvidhya.com/blog/2019/06/comprehensive-guide-text-summarization-using-deep-learning-python/" %}

Simple ideas here

{% embed url="https://stackabuse.com/text-summarization-with-nltk-in-python/" %}

Lots of methods and their links to papers

{% embed url="https://towardsdatascience.com/data-scientists-guide-to-summarization-fc0db952e363" %}

Implement your own abstractive deep nn

{% embed url="https://github.com/aravindpai/How-to-build-own-text-summarizer-using-deep-learning/blob/master/How\_to\_build\_own\_text\_summarizer\_using\_deep\_learning.ipynb" %}

PEGASUS by Google:

{% embed url="https://ai.googleblog.com/2020/06/pegasus-state-of-art-model-for.html" %}





