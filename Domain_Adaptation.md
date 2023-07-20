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
