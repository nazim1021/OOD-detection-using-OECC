Use the steps below to replicate the results of <b>Table 3</b> and <b>Table 6</b> of the paper [_Outlier Exposure with Confidence Control for Out-of-Distribution Detection_](https://arxiv.org/abs/1906.03509).

## Download Datasets
* '20 Newsgroups' train and test datasets are already provided in the files '20ng-train.txt' and '20ng-test.txt', respectively. Please keep at their given location. 

* 'Wikitext2' dataset that is for fine-tuning with the OECC loss finction is already provided in the file 'wikitext_sentences'. Please keep it at its given location.

* 'Yelp' dataset is already provided in the 'yelp.csv' file. Please keep it at its given location.

* 'SNLI' and 'IMDB' datasets will be automatically downloaded by torchtext by running any of the files `Test_eval_OOD_XYZ.ipynb` where XYZ can be '20ng', 'trec', 'sst'.

* 'TREC' and 'SST' datasets will be automatically downloaded by torchtext by running the file `baseline_train.ipynb` by changing the corresponding argument of in-distribution dataset to 'trec' or 'sst', respectively.


## How to Run
The snapshots of the evaluation results presented in <b>Table 3</b> and <b>Table 6</b> of the paper can be found in the folders `./results/XYZ/OECC/wikitext2/OECC_eval_results.txt` where XYZ can be '20ng', 'trec', 'sst'. 

* To reproduce the results presented in <b>Table 3</b> and <b>Table 6</b> of the paper, please run `Test_eval_OOD_XYZ.ipynb` where XYZ can be '20ng', 'trec', 'sst'. 

* To validate different values of the hyperparameters of the OECC loss function as mentioned in <b>Appendix B.2</b> of the paper, please run `Validation_eval_OOD_XYZ.ipynb` where XYZ can be '20ng', 'trec', 'sst'. 

* To train a baseline GRU model with 2 layers, please run `baseline_train.ipynb` changing the corresponding argument for '20ng', 'trec' or 'sst'.

* To fine-tune the baseline model with the OECC loss function, please run `fine_tune_OECC.ipynb` changing the corresponding argument for '20ng', 'trec' or 'sst'.
