# Deep Learning


#### 2019 - Dettmers and Zettlemoyers - [Sparse Networks from Scratch: Faster Training without Losing Performance](https://arxiv.org/abs/1907.04840)

Introduce sparce learning algorithm. Dring course of training, for each layer weights with low momentum are pruned, and new weights are formed following the distribution of layers' momentums.
Intuitively, the goal is to take weights from less efficient layers and redistribute them to weight-efficient layers, as the authors argue that the aggregated momentum of weights in each layer
should reflect how good each layer is at reducing the error consistently. The original amount of wheights is left as a crucial hyperparameter, balancing the accuracy and runtime of the network.
The paper also boasts significant training time gains, that are only theoretical at the time of publishing as GPUs are not optimized for sparse operations. 
