# Domain Adaptation


#### 2018 - Saito et al. - [Maximum Classifier Discrepancy for Unsupervised Domain Adaptation](https://arxiv.org/abs/1712.02560)

[Official Pytorch implementation](https://github.com/mil-tokyo/MCD_DA/tree/master/classification)

This works tackle the UDA problem using an adversarial method. They use two classifiers and one generator; both source and domain data go through the generator.
The training proceeds in three steps:
a. Train the classifiers and generator on the source domain with the classification loss.
b. Train the classifiers to minimize classification loss on source and maximise the discrepancy on target
c. Train the generator to minimize target discrepancy. This step is repeated k times (hyperparameter) witthe same data sample.


#### 2020 - Chen et al. - [HoMM: Higher-order Moment Matching for Unsupervised Domain Adaptation](https://arxiv.org/abs/1912.11976)

[Official Tensorflow implementation](https://github.com/chenchao666/HoMM-Master)

The authors aim at minimizing the discrepancy of feature distributions between the domains.
They show that first order HoMM is equivalent to MMD (Maximum Mean Discrepancy) and second order to CORAL (Correlation Alignment).
They argue that using a higher moment order help better approximate non-Gaussian distribution, and outperforms previous discrepancy measures while integrating them in their framework.
The method can be further improved by assigning pseudo-labels to the target domain.


#### 2020 - Liang et al. - [Do We Really Need to Access the Source Data? Source Hypothesis Transfer for Unsupervised Domain Adaptation](https://arxiv.org/abs/2002.08546)



#### 2022 - Xu et al. - [CDTrans: Cross-domain Transformer for Unsupervised Domain Adaptation](https://arxiv.org/abs/2109.06165v4)

[Official Pytorch implementation](https://github.com/CDTrans/CDTrans)

One of the first attempts to solve UDA with vision transformers.
Authors show that the cross attention of transformer models is less sensitive to pseudo-label noise than CNNs.
They designed a model using three branches, for source data, target data and feature alignment. 

Additionally, they propose a method to generate pseudo-labels
First, generate pairs by associating each image in both datasets to their closest counterpart (in the feature space)
Then, filter the pairs by assigning pseudo-labels to target data:
- assign a first label with a source-trained classifier
- compute the centers for each class and assign the final pseudo-label based on the closest class center
- discard pairs if the source label and target pseudo-label are different.

<details>
<summary>Bibtex</summary>
```
@inproceedings{XuCDTrans2022,
  title     = {{CDT}rans: Cross-domain Transformer for Unsupervised Domain Adaptation},
  author    = {Tongkun Xu and Weihua Chen and Pichao WANG and Fan Wang and Hao Li and Rong Jin},
  booktitle = {International Conference on Learning Representations},
  year      = {2022},
  url       = {https://openreview.net/forum?id=XGzk5OKWFFc}
}
```
</details>

#### 2023 - Zhang et al. - [Free Lunch for Domain Adversarial Training: Environment Label Smoothing](https://arxiv.org/abs/2302.00194v1)

[Official Pytorch implementation](https://github.com/yfzhang114/Environment-Label-Smoothing)

DA using adversarial methods is difficult because of the balance between discriminator and generator training. 
This work encourages the discriminator to output soft probabilities, which in turn improve training stability, local convergence, and robustness to noisy environment labels.

<details>
<summary>Bibtex</summary>
```
@inproceedings{ZhangELS2023,
  title     = {Free Lunch for Domain Adversarial Training: Environment Label Smoothing},
  author    = {YiFan Zhang and Xue Wang and Jian Liang and Zhang Zhang and Liang Wang and Rong Jin and Tieniu Tan},
  booktitle = {The Eleventh International Conference on Learning Representations },
  year      = {2023},
  url       = {https://openreview.net/forum?id=GPTjnA57h_3}
}
```
</details>

#### 2023 - Zhu et al. - [Patch-Mix Transformer for Unsupervised Domain Adaptation: A Game Perspective](https://arxiv.org/abs/2303.13434)

[Official Pytorch implementation](https://github.com/JinjingZhu/PMTrans)

Introduce the PMTrans model for UDA. They proposed a ViT-based model that creates an intermediate domain between source and target by sampling patches from both datasets.
The approach effectively solves cases where there is a large gap between the two domains.

#### 2023 - Yang et al. - [TVT: Transferable Vision Transformer for Unsupervised Domain Adaptation](https://arxiv.org/abs/2108.05988)

[Official Pytorch implementation](https://github.com/uta-smile/TVT)

<details>
<summary>Bibtex</summary>
```
@inproceedings{YangTVT2023,
  author    = {J. Yang and J. Liu and N. Xu and J. Huang},
  booktitle = {2023 IEEE/CVF Winter Conference on Applications of Computer Vision (WACV)},
  title     = {TVT: Transferable Vision Transformer for Unsupervised Domain Adaptation},
  year      = {2023},
  pages     = {520-530},
  doi       = {10.1109/WACV56688.2023.00059},
  url       = {https://doi.ieeecomputersociety.org/10.1109/WACV56688.2023.00059},
  publisher = {IEEE Computer Society}
}
```
</details>