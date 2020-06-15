Use the steps below to replicate the results of <b>Table 5</b> and <b>Table 6</b> of the paper [_Outlier Exposure with Confidence Control for Out-of-Distribution Detection_](https://arxiv.org/abs/1906.03509).

## Download Out-of-Distribution (OOD) Datasets
Tiny-ImageNet and LSUN datasets can be downloaded by the following links:

* [Tiny-ImageNet (resize)](https://www.dropbox.com/s/kp3my3412u5k9rl/Imagenet_resize.tar.gz)
* [LSUN (resize)](https://www.dropbox.com/s/moqh2wh8696c3yl/LSUN_resize.tar.gz)

Place them to `./data/`.

## Download Pre-Trained and Fine-Tuned Models
For our experiments, we used the ResNet-34 (Table 5) and the Densenet-100 (Table 6) network architectures. The Pre-Trained Densenet-100 models for CIFAR-10, CIFAR-100 and SVHN datasets are provided in `./pre_trained/`. The Fine-Tuned Densenet-100 models for CIFAR-10, CIFAR-100 and SVHN datasets are provided in `./results/Zero_Shot`. The Pre-Trained ResNet-34 models for CIFAR-10, CIFAR-100 and SVHN datasets can be downloaded by the following link: 

* [Pre-Trained ResNet models](https://www.dropbox.com/sh/kktuiar3parraaq/AABh1Ar5XoPi_25LAlqADCo7a/zeroshot_ood_experiments/pre_trained?dl=0&subfolder_nav_tracking=1)

The Pre-Trained models are also fine-tuned using the Outlier Exposure with Confidence Control (OECC) loss function. The Fine-Tuned models for CIFAR-10, CIFAR-100 and SVHN datasets can be downloaded by the following link:

* [Fine-Tuned ResNet models](https://www.dropbox.com/sh/kktuiar3parraaq/AAC_7jnxtdfJinR8_SulSxWua/zeroshot_ood_experiments/results/Zero_Shot?dl=0&subfolder_nav_tracking=1)
