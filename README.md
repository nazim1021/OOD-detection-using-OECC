# OOD-detection-using-OECC

This repository contains the essential code for the paper [_Outlier Exposure with Confidence Control for Out-of-Distribution Detection_](https://arxiv.org/abs/1906.03509) (arXiv 2019).


## 1. Visualize the idea behind OECC

<p float="left">
  <img src="/baseline_cifar10_places365_distribution.png" width="410" /> 
  <img src="/OECC_cifar10_places365_distribution.png" width="410" />
</p>
<b>Figure.</b> Histogram of softmax probabilities with CIFAR-10 as in-distribution data D<sub>in</sub> and Places365 as Out-of-Distribution (OOD) data D<sub>out</sub>. Note that D<sub>in</sub> and D<sub>out</sub> are disjoint. <b>Left:</b> Standard maximum softmax probability detector. <b>Right:</b> Maximum softmax probability detector using OECC.


## 2. What is Outlier Exposure with Confidence Control (OECC)?
[_Outlier Exposure (OE)_](https://github.com/hendrycks/outlier-exposure) is a technique that uses out-of-distribution data so that the model learns how to distinguish in- and out-of-distribution samples. This technique has been shown that it can generalize to new distibutions. To learn how to distinguish in- and out-of-distribution samples, [Outlier Exposure with Confidence Control (OECC)](https://arxiv.org/abs/1906.03509) makes a NN to be highly uncertain for OOD samples by producing a uniform distribution at the output of the softmax layer. At the same time, it also makes it to make predictions for in-distribution samples with an average confidence close to its training accuracy, i.e. it controls its confidence. 

The overall OECC loss function outperforms the previous SOTA results in OOD detection with OE both in image and text classification tasks. Additionally, we experimentally show in the [paper](https://arxiv.org/abs/1906.03509) that by combining OECC with Distance-Based Post-Training (DBPT) methods for OOD detection like the [_Mahalanobis Detector_](https://github.com/pokaxpoka/deep_Mahalanobis_detector), one can achieve SOTA results in the OOD detection task.   


## 3. Citation

If you find this useful in your research, please consider citing:

    @article{papadopoulos2020OECC,
        title={Outlier Exposure with Confidence Control for Out-of-Distribution Detection},
        author={Aristotelis-Angelos Papadopoulos and Mohammad Reza Rajati and Nazim Shaikh and Jiamian Wang},
        year={2019},
        journal = {arXiv preprint arXiv:1906.03509},
        eprint={1906.03509},
        archivePrefix={arXiv},
        primaryClass={cs.LG}
    }
    
    
## 4. Code References

A part of the code has been based on the publicly available codes of [_Outlier Exposure_](https://github.com/hendrycks/outlier-exposure) and [_Mahalanobis_](https://github.com/pokaxpoka/deep_Mahalanobis_detector).
