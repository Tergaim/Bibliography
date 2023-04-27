# Person Re-Identification

Person Re-Identification is a computer vision task in which the goal is to match a person's identity across different cameras or locations in a video or image sequence.
It involves detecting and tracking a person and then using features such as appearance, body shape, and clothing to match their identity in different frames.
The goal is to associate the same person across multiple camera views in a robust and efficient manner.

#### 2017 - Zhong et al - [Re-ranking Person Re-identification with k-reciprocal Encoding](https://arxiv.org/abs/1701.08398)



#### 2022 - Takeuchi et al - [Unsupervised Domain-Adaptive Person Re-Identification with Multi-Camera Constraints](https://arxiv.org/abs/2210.13999)

Work on reducing the loss in performance incurred when using a model in a different environment from training. 
Their method, ECA-Net, is meant for environments with overlapping camera views.
The model uses two image datasets: the source domain data (with person ID labels) and target domain data that contains only person-pair data obtained through overlapping cameras.
A CNN is used to extract features from an image, and the Jaccard distance is used to compare two persons.
The model can be trained using triplet loss on the source dataset, and identity loss on the Jaccard distance for pairs in the target domain. 
