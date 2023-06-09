# Person Re-Identification

Person Re-Identification is a computer vision task in which the goal is to match a person's identity across different cameras or locations in a video or image sequence.
It involves detecting and tracking a person and then using features such as appearance, body shape, and clothing to match their identity in different frames.
The goal is to associate the same person across multiple camera views in a robust and efficient manner.

#### 2017 - Zhong et al - [Re-ranking Person Re-identification with k-reciprocal Encoding](https://arxiv.org/abs/1701.08398)

Idea: if a neighbour A of the query Q is a true positive, then Q should appear when querying the neighbours of A.
The authors use this as the basis of k-reciprocal encoding. The resulting distance between the query and the results is a weighted average of the regular distance between vectors, and the Jaccard distance between k-NN sets.
This requires no learning nor labels and can be added to any other Re-ID method.

#### 2021 - Wieczorek et al. - [On the Unreasonable Effectiveness of Centroids in Image Retrieval](https://arxiv.org/abs/2104.13643)

[Official Pytorch-lightning implementation](https://github.com/mikwieczorek/centroids-reid/tree/main)

Work on representing each class by an aggregated embedding. This simplifies time and memory complexity, and reduces the variance due to changes in view angles, lighting, etc. While the idea itself is not new, it is usually only applied during training; the authors of this work show that using mean centroid representations during retrieval is beneficial to the system's performance.


#### 2022 - Takeuchi et al - [Unsupervised Domain-Adaptive Person Re-Identification with Multi-Camera Constraints](https://arxiv.org/abs/2210.13999)

Work on reducing the loss in performance incurred when using a model in a different environment from training. 
Their method, ECA-Net, is meant for environments with overlapping camera views.
The model uses two image datasets: the source domain data (with person ID labels) and target domain data that contains only person-pair data obtained through overlapping cameras.
A CNN is used to extract features from an image, and the Jaccard distance is used to compare two persons.
The model can be trained using triplet loss on the source dataset, and identity loss on the Jaccard distance for pairs in the target domain. 
