Use the steps below to replicate the results of <b>Table 4</b> of the paper [_Outlier Exposure with Confidence Control for Out-of-Distribution Detection_](https://arxiv.org/abs/1906.03509).

## Download Out-of-Distribution (OOD) Datasets
Tiny-ImageNet and LSUN datasets can be downloaded by the following links:

* [Tiny-ImageNet (resize)](https://www.dropbox.com/s/kp3my3412u5k9rl/Imagenet_resize.tar.gz)
* [LSUN (resize)](https://www.dropbox.com/s/moqh2wh8696c3yl/LSUN_resize.tar.gz)

Place them to `./data/`.

## Download Pre-Trained and Fine-Tuned Models
For our experiments, we used the ResNet-34 network architecture. The Pre-Trained models for CIFAR-10, CIFAR-100 and SVHN datasets can be downloaded by the following link: 

* [Pre-Trained ResNet models](https://www.dropbox.com/sh/zsossiqfbughrxz/AAAgN-ZJzzDBXH2csQCP-bt9a?dl=0)

The Pre-Trained models are also fine-tuned using the Outlier Exposure with Confidence Control (OECC) loss function. The Fine-Tuned models for CIFAR-10, CIFAR-100 and SVHN datasets can be downloaded by the following link:

* [Fine-Tuned ResNet models](https://www.dropbox.com/sh/9go8i8v6wiujdrc/AADIr9foN7rpBAMiCJDVaQ7Fa?dl=0)

After downloading, place the Pre-Trained models to `./pre_trained/` and the Fine-Tuned models to `./results/Mahal_OECC_tune/`.

## How to Run
* To evaluate a Fine-Tuned ResNet model, please run the notebook `OOD_Generate_Mahalanobis.ipynb` by choosing the appropriate argument 'cifar10', 'cifar100', 'svhn'. This will create a `./output/` folder. Then, run the notebook `OOD_Regression_Mahalanobis.ipynb`.


