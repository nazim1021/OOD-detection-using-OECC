Use the steps below to replicate the results of CIFAR experiments of our paper [_Outlier Exposure with Confidence Control for Out-of-Distribution Detection_](https://arxiv.org/abs/1906.03509).

## Download Datasets

- The in-distribution datasets - CIFAR100 or CIFAR10 gets automatically downloaded while running dataset section in any of the notebooks of the current folder.
- Out-of-Distribution datasets can be downloaded by the given links in the parent README file. After downloading, please place them in the parent directory itself.


## How to Run
The snapshots of the evaluation results presented in <b>Table 1</b> and <b>Table 5</b> of the paper can be found in the folders `./results/OECC_tune/`.

* To reproduce the results, please run `test_cifar.ipynb`. 

* To train a baseline model, please run `baseline_cifar.ipynb`.

* To fine-tune the baseline model with the OECC loss function, please run `OECC_tune_cifar.ipynb`.
