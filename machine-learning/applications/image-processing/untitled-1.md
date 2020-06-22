# Face recognition

### What is it

The idea is to recognize a face from a photo, useful in many scenarios. The first step is though to find a way to represent a face. There have been many attempts for this, most of which tried to mimic the way human persumably does it, i.e., recoginzing face components \(see [here](https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78) the history\). The most recent method has been very succesful, which generates a characterisitc vector out of faces automatically \(i.e., embedding faces\). The vector does not explicitly map to face features. 

![](../../../.gitbook/assets/image%20%2816%29.png)

Consider a neural network that takes a face image and generates this vector. What we want is that if we feed the network with the face of one particular person, in any pose, the generated vectors are fairly similar vector. But the vectors generated for two different people should be fairly different. 

![](../../../.gitbook/assets/image%20%2817%29.png)









{% embed url="https://medium.com/@ageitgey/machine-learning-is-fun-part-4-modern-face-recognition-with-deep-learning-c3cffc121d78" %}

See also 

{% embed url="https://www.cv-foundation.org/openaccess/content\_cvpr\_2015/app/1A\_089.pdf" %}



### Implementation

Pretty stable and fast library

{% embed url="https://pypi.org/project/face-recognition/" %}







