Use the steps below to replicate the results of SVHN experiments of our paper [_Outlier Exposure with Confidence Control for Out-of-Distribution Detection_](https://arxiv.org/abs/1906.03509).

## Download Datasets

- The in-distribution dataset - SVHN can be downloaded from http://ufldl.stanford.edu/housenumbers/. Download the .mat files and place them in the same directory as SVHN notebooks.
- Out-of-Distribution datasets can be downloaded by the given links in the parent README file. After downloading, please place them in the parent directory itself.


## How to Run
The snapshots of the evaluation results presented in <b>Table 1</b> and <b>Table 5</b> of the paper can be found in the folder `./results/OECC_tune/`.

* To reproduce the results, please run `test_SVHN.ipynb`. 

* To train a baseline model, please run `baseline_SVHN.ipynb`.

* To fine-tune the baseline model with the OECC loss function, please run `OECC_tune_SVHN.ipynb`.
