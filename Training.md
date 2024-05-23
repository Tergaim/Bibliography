# Training & Fine-Tuning

## Data Augmentation


#### 2020 - Cubuk et al. - [RandAugment: Practical automated data augmentation with a reduced search space](https://arxiv.org/abs/1909.13719)

[Non-official Pytorch implementation](https://github.com/ildoonet/pytorch-randaugment)

RandAugment has a significantly reduced search space which allows it to be trained on the target task with no need for a separate proxy task compared to previous augmentation methods. Furthermore, due to the parameterization, the regularization strength may be tailored to different model and dataset sizes. RandAugment can be used uniformly across different tasks and datasets and works out of the box.  Finally, due to its interpretable hyperparameter, RandAugment may be used to investigate the role of data augmentation with varying model and dataset size. 

<details>
<summary>Bibtex</summary>
 
```
@inproceedings{CubukRandAugment2020,
 author = {Cubuk, Ekin Dogus and Zoph, Barret and Shlens, Jon and Le, Quoc},
 booktitle = {Advances in Neural Information Processing Systems},
 editor = {H. Larochelle and M. Ranzato and R. Hadsell and M.F. Balcan and H. Lin},
 pages = {18613--18624},
 publisher = {Curran Associates, Inc.},
 title = {RandAugment: Practical Automated Data Augmentation with a Reduced Search Space},
 url = {https://proceedings.neurips.cc/paper_files/paper/2020/file/d85b63ef0ccb114d0a3bb7b7d808028f-Paper.pdf},
 volume = {33},
 year = {2020}
}
```

</details>

## Fine-Tuning


#### 2021 - Wortsman et al. - [Robust fine-tuning of zero-shot models](https://arxiv.org/abs/2109.01903)

[Official Pytorch implementation](https://github.com/mlfoundations/wise-ft) 

Large pre-trained models such as CLIP or ALIGN offer consistent accuracy across a range of data distributions when performing zero-shot inference (i.e., without fine-tuning on a specific dataset). Although existing fine-tuning methods substantially improve accuracy on a given target distribution, they often reduce robustness to distribution shifts. We address this tension by introducing a simple and effective method for improving robustness while fine-tuning: ensembling the weights of the zero-shot and fine-tuned models (WiSE-FT). Compared to standard fine-tuning, WiSE-FT provides large accuracy improvements under distribution shift, while preserving high accuracy on the target distribution. These improvements come at no additional computational cost during fine-tuning or inference.


<details>
<summary>Bibtex</summary>
 
```
@InProceedings{WortsmanFineTuning2022,
    author    = {Wortsman, Mitchell and Ilharco, Gabriel and Kim, Jong Wook and Li, Mike and Kornblith, Simon and Roelofs, Rebecca and Lopes, Raphael Gontijo and Hajishirzi, Hannaneh and Farhadi, Ali and Namkoong, Hongseok and Schmidt, Ludwig},
    title     = {Robust Fine-Tuning of Zero-Shot Models},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
    month     = {June},
    year      = {2022},
    pages     = {7959-7971}
}
```

</details>


#### 2022 - Wortsman et al. - [Model soups: averaging weights of multiple fine-tuned models improves accuracy without increasing inference time](https://arxiv.org/abs/2203.05482)

[Official Pytorch implementation](https://github.com/mlfoundations/model-soups)

We show that averaging the weights of multiple models fine-tuned with different hyperparameter configurations often improves accuracy and robustness. Unlike a conventional ensemble, we may average many models without incurring any additional inference or memory costs -- we call the results "model soups.". Furthermore, we show that the model soup approach extends to multiple image classification and natural language processing tasks, improves out-of-distribution performance, and improves zero-shot performance on new downstream tasks. Finally, we analytically relate the performance similarity of weight-averaging and logit-ensembling to flatness of the loss and confidence of the predictions, and validate this relation empirically. 

<details>
<summary>Bibtex</summary>
 
```
@InProceedings{WortsmanSoup2022,
  title = 	 {Model soups: averaging weights of multiple fine-tuned models improves accuracy without increasing inference time},
  author =       {Wortsman, Mitchell and Ilharco, Gabriel and Gadre, Samir Ya and Roelofs, Rebecca and Gontijo-Lopes, Raphael and Morcos, Ari S and Namkoong, Hongseok and Farhadi, Ali and Carmon, Yair and Kornblith, Simon and Schmidt, Ludwig},
  booktitle = 	 {Proceedings of the 39th International Conference on Machine Learning},
  pages = 	 {23965--23998},
  year = 	 {2022},
  editor = 	 {Chaudhuri, Kamalika and Jegelka, Stefanie and Song, Le and Szepesvari, Csaba and Niu, Gang and Sabato, Sivan},
  volume = 	 {162},
  series = 	 {Proceedings of Machine Learning Research},
  month = 	 {17--23 Jul},
  publisher =    {PMLR},
  pdf = 	 {https://proceedings.mlr.press/v162/wortsman22a/wortsman22a.pdf},
  url = 	 {https://proceedings.mlr.press/v162/wortsman22a.html}
}
```

</details>
