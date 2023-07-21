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

#### 2021 - Xu et al. - [CDTrans: Cross-domain Transformer for Unsupervised Domain Adaptation](https://arxiv.org/abs/2109.06165v4)

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


#### 2023 - Zhang et al. - [Free Lunch for Domain Adversarial Training: Environment Label Smoothing](https://arxiv.org/abs/2302.00194v1)

[Official Pytorch implementation](https://github.com/yfzhang114/Environment-Label-Smoothing)

DA using adversarial methods is difficult because of the balance between discriminator and generator training. 
This work encourages the discriminator to output soft probabilities, which in turn improve training stability, local convergence, and robustness to noisy environment labels.


#### 2023 - Zhu et al. - [Patch-Mix Transformer for Unsupervised Domain Adaptation: A Game Perspective](https://arxiv.org/abs/2303.13434)

[Official Pytorch implementation](https://github.com/JinjingZhu/PMTrans)

Introduce the PMTrans model for UDA. They proposed a ViT-based model that creates an intermediate domain between source and target by sampling patches from both datasets.
The approach effectively solves cases where there is a large gap between the two domains.
