# Action Recognition

In an action recognition problem, we want to identify actions performed by a (generally, human) agent. Most methods can be classified in three categories, depending on whether they use the input video, skeleton information (that requires an additional detection model) or both.

#### 2020 - Obinata and Yamamoto - [Temporal Extension Module fo Skeleton-Based Action Recognition](https://arxiv.org/abs/2003.08951) 

Action recognition based on Graph Convolutional Network, using temporal graph of the skeleton. 
Usually, a joint is connected to the neighbouring joint in the same frame, and to the same joint in frame n+-1.
In this work, information about neighbouring joints in frames n+-1 is also used. 
They show that not only is this method efficient, but it can be applied to improve other GCN-based methods' accuracy.

#### 2023 - Ahn et al. - [STAR-Transformer: A Spatio-Temporal Cross Atention Transformer for Human Action Recognition](https://arxiv.org/abs/2210.07503)

Propose propose a model that can effectively represent two cross-modal features as a recognizable vector, using both skeleton information and videos.
Seems to be the first attempt to do this with transformers instead of more traditional approaches.
