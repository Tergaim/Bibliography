# Loss functions


## Noisy Labels

#### 2018 - Zhang and Sabuncu - [Generalized Cross Entropy Loss for Training Deep Neural Networks with Noisy Labels](https://arxiv.org/abs/1805.07836)

[Unofficial Pytorch implementation](https://github.com/AlanChou/Truncated-Loss)

Authors show that Mean Absolute Error (MAE), while more robust than the Categorical Cross-Entropy (CCE), can lead to slower convergence and worse final performance. They propose the "negative Box-Cox transformation" as a generalization of both CCE and MAE, and experiment on the CIFAR dataset with corrupted labels.

<details>
<summary>Bibtex</summary>
```
@inproceedings{10.5555/3327546.3327555,
author = {Zhang, Zhilu and Sabuncu, Mert R.},
title = {Generalized Cross Entropy Loss for Training Deep Neural Networks with Noisy Labels},
year = {2018},
publisher = {Curran Associates Inc.},
booktitle = {Proceedings of the 32nd International Conference on Neural Information Processing Systems},
pages = {8792–8802},
numpages = {11},
series = {NIPS'18}
}
```
</details>



#### 2021 - Zhang et al. - [Simple and Robust Loss Design for Multi-Label Learning with Missing Labels](https://arxiv.org/abs/2112.07368)

[Official Pytorch implementation](https://github.com/xinyu1205/robust-loss-mlml)

Design two loss functions to handle missing labels to reduce the impact of false negatives. 

<details>
<summary>Bibtex</summary>
```
@article{ZhangHill2021,
  author       = {Youcai Zhang and Yuhao Cheng and Xinyu Huang and Fei Wen and Rui Feng and Yaqian Li and Yandong Guo},
  title        = {Simple and Robust Loss Design for Multi-Label Learning with Missing Labels},
  journal      = {CoRR},
  volume       = {abs/2112.07368},
  year         = {2021},
  eprinttype    = {arXiv},
  eprint       = {2112.07368},
  timestamp    = {Mon, 03 Jan 2022 15:45:35 +0100},
}
```
</details>

## Links

[Mathematical derivation of 0-1 loss for PUL](https://e-dorigatti.github.io/math/deep%20learning/2021/10/16/pu-loss.html)