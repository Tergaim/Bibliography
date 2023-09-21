# Noisy Labels

#### 2021 - Zhou et al. - [Robust Curriculum Learning: from clean label detection to noisy label self-correction](https://openreview.net/forum?id=lmTWnm3coJJ)

In this paper, we propose a smooth transition and interplay between these two strategies as a curriculum that selects training samples dynamically. In particular, we start with learning from clean data and then gradually move to learn noisy-labeled data with pseudo labels produced by a time-ensemble of the model and data augmentations. Instead of using the instantaneous loss computed at the current step, our data selection is based on the dynamics of both the loss and output consistency for each sample across historical steps and different data augmentations, resulting in more precise detection of both clean labels and correct pseudo labels. 

<details>
<summary>Bibtex</summary>
```
@inproceedings{ZhouRobust2021,
title={Robust Curriculum Learning: from clean label detection to noisy label self-correction},
author={Tianyi Zhou and Shengjie Wang and Jeff Bilmes},
booktitle={International Conference on Learning Representations},
year={2021},
url={https://openreview.net/forum?id=lmTWnm3coJJ}
}
```
</details>

#### 2023 - Xiao et al. - [ProMix: Combating Label Noise via Maximizing Clean Sample Utility](https://arxiv.org/abs/2207.10276v4)

[Official Pytorch implementation](https://github.com/justherozen/promix)

Recent state-of-the-art approaches employ specific selection mechanisms to separate clean and noisy samples and then apply Semi-Supervised Learning (SSL) techniques for improved performance. However, the selection step mostly provides a medium-sized and decent-enough clean subset, which overlooks a rich set of clean samples. To fulfill this, we propose a novel framework ProMix that attempts to maximize the utility of clean samples for boosted performance. Key to our method, we propose a matched high confidence selection technique that selects those examples with high confidence scores and matched predictions with given labels to dynamically expand a base clean sample set. To overcome the potential side effect of excessive clean set selection procedure, we further devise a novel SSL framework that is able to train balanced and unbiased classifiers on the separated clean and noisy samples

<details>
<summary>Bibtex</summary>
```
@inproceedings{XiaoProMix2023,
  title     = {ProMix: Combating Label Noise via Maximizing Clean Sample Utility},
  author    = {Xiao, Ruixuan and Dong, Yiwen and Wang, Haobo and Feng, Lei and Wu, Runze and Chen, Gang and Zhao, Junbo},
  booktitle = {Proceedings of the Thirty-Second International Joint Conference on
               Artificial Intelligence, {IJCAI-23}},
  publisher = {International Joint Conferences on Artificial Intelligence Organization},
  editor    = {Edith Elkind},
  pages     = {4442--4450},
  year      = {2023},
  month     = {8},
  note      = {Main Track},
  doi       = {10.24963/ijcai.2023/494},
  url       = {https://doi.org/10.24963/ijcai.2023/494},
}
```
</details>