# Sequence 2 sequence

## Introduction

Sequence-to-sequence learning \(Seq2Seq\) is about training models to convert sequences from one domain \(e.g. sentences in English\) to sequences in another domain \(e.g. the same sentences translated to French\).

```text
"the cat sat on the mat" -> [Seq2Seq model] -> "le chat etait assis sur le tapis"
```

Using RNN/LSTM

Using Convnet1D

## Seq2seq using RNN

### How it works



![](../../../.gitbook/assets/image%20%2814%29.png)





![Source &#x2013; https://github.com/google/seq2seq](../../../.gitbook/assets/s2s.gif)

### State-of-the-art

See T5 [here](https://arxiv.org/abs/1910.10683)

### Implementation

* See [this link](https://blog.keras.io/a-ten-minute-introduction-to-sequence-to-sequence-learning-in-keras.html) for an implementation in Keras from scratch
* See also [this](https://www.analyticsvidhya.com/blog/2018/03/essentials-of-deep-learning-sequence-to-sequence-modelling-with-attention-part-i/) for another implementation with Attention mechanism
* See T5 by Google [here](https://ai.googleblog.com/2020/02/exploring-transfer-learning-with-t5.html) which is a hybrid of many methods



![](../../../.gitbook/assets/image3.gif)

* 
### Further reading

{% embed url="https://www.analyticsvidhya.com/blog/2018/03/essentials-of-deep-learning-sequence-to-sequence-modelling-with-attention-part-i/" %}













