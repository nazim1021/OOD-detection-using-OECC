## 1. Outlier Exposure with Confidence Control (OECC)
[_Outlier Exposure (OE)_](https://github.com/hendrycks/outlier-exposure) is a technique that uses out-of-distribution data so that the model learns how to distinguish in- and out-of-distribution samples. This technique has been shown that it can generalize to new distibutions. To learn how to distinguish in- and out-of-distribution samples, OECC makes a NN to be highly uncertain <b>for OOD samples</b> by producing <b>a uniform distribution at the output of the softmax layer</b>. At the same time, it also makes it to make predictions <b>for in-distribution samples</b> with <b>an average confidence close to its training accuracy</b>, i.e. it controls its confidence. 

The overall OECC loss function outperforms the previous SOTA results in OOD detection with OE both in image and text classification tasks. Additionally, we experimentally show that by combining OECC with Distance-Based Post-Training (DBPT) methods for OOD detection like the [_Mahalanobis Detector_](https://github.com/pokaxpoka/deep_Mahalanobis_detector), one can achieve SOTA results in the OOD detection task. 


## 2. Visualize the idea behind OECC

<p float="left">
  <img src="/baseline_cifar10_places365_distribution.png" width="410" /> 
  <img src="/OECC_cifar10_places365_distribution.png" width="410" />
</p>
<b>Figure.</b> Histogram of softmax probabilities with CIFAR-10 as in-distribution data D<sub>in</sub> and Places365 as Out-of-Distribution (OOD) data D<sub>out</sub>. Note that D<sub>in</sub> and D<sub>out</sub> are disjoint. <b>Left:</b> Standard maximum softmax probability detector. <b>Right:</b> Maximum softmax probability detector using OECC.  
    

## 3. Download Datasets

Some of the less common datasets can be downloaded by the following links: [80 Million Tiny Images](http://horatio.cs.nyu.edu/mit/tiny/data/tiny_images.bin), [Icons-50](https://github.com/hendrycks/robustness),
[Textures](https://www.robots.ox.ac.uk/~vgg/data/dtd/), [Chars74K](http://www.ee.surrey.ac.uk/CVSSP/demos/chars74k/EnglishImg.tgz), and [Places365](http://places2.csail.mit.edu/download.html).


## 4. How to Run

Each folder has its own separate README file with full details describing how to run the provided code.


## 5. Code References

A part of the code has been based on the publicly available codes of [_Outlier Exposure_](https://github.com/hendrycks/outlier-exposure) and [_Mahalanobis_](https://github.com/pokaxpoka/deep_Mahalanobis_detector).
