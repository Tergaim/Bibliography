# Domain Adaptation



#### 2020 - Chen et al. - [HoMM: Higher-order Moment Matching for Unsupervised Domain Adaptation](https://arxiv.org/abs/1912.11976)

[Official Tensorflow implementation](https://github.com/chenchao666/HoMM-Master)

The authors aim at minimizing the discrepancy of feature distributions between the domains.
They show that first order HoMM is equivalent to MMD (Maximum Mean Discrepancy) and second order to CORAL (Correlation Alignment).
They argue that using a higher moment order help better approximate non-Gaussian distribution, and outperforms previous discrepancy measures while integrating them in their framework.
The method can be further improved by assigning pseudo-labels to the target domain.
