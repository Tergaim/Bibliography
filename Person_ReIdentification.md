# Person Re-Identification

Person Re-Identification is a computer vision task in which the goal is to match a person's identity across different cameras or locations in a video or image sequence.
It involves detecting and tracking a person and then using features such as appearance, body shape, and clothing to match their identity in different frames.
The goal is to associate the same person across multiple camera views in a robust and efficient manner.

#### 2017 - Zhong et al - [Re-ranking Person Re-identification with k-reciprocal Encoding](https://arxiv.org/abs/1701.08398)

[Official Caffee implementation](https://github.com/zhunzhong07/person-re-ranking)

Idea: if a neighbour A of the query Q is a true positive, then Q should appear when querying the neighbours of A.
The authors use this as the basis of k-reciprocal encoding. The resulting distance between the query and the results is a weighted average of the regular distance between vectors, and the Jaccard distance between k-NN sets.
This requires no learning nor labels and can be added to any other Re-ID method.

<details>
<summary>Bibtex</summary>
  
```
@INPROCEEDINGS {ZhongReRanking2017,
author = {Z. Zhong and L. Zheng and D. Cao and S. Li},
booktitle = {2017 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
title = {Re-ranking Person Re-identification with k-Reciprocal Encoding},
year = {2017},
issn = {1063-6919},
pages = {3652-3661},
doi = {10.1109/CVPR.2017.389},
url = {https://doi.ieeecomputersociety.org/10.1109/CVPR.2017.389},
publisher = {IEEE Computer Society},
address = {Los Alamitos, CA, USA},
month = {jul}
}
```

</details>

#### 2021 - Wieczorek et al. - [On the Unreasonable Effectiveness of Centroids in Image Retrieval](https://arxiv.org/abs/2104.13643)

[Official Pytorch-lightning implementation](https://github.com/mikwieczorek/centroids-reid/tree/main)

Work on representing each class by an aggregated embedding. This simplifies time and memory complexity, and reduces the variance due to changes in view angles, lighting, etc. While the idea itself is not new, it is usually only applied during training; the authors of this work show that using mean centroid representations during retrieval is beneficial to the system's performance.

<details>
<summary>Bibtex</summary>
  
```
@inproceedings{WieczorekCentroids2021,
author = {Wieczorek, Miko\l{}aj and Rychalska, Barbara and D\k{a}browski, Jacek},
title = {On The Unreasonable Effectiveness Of Centroids In Image Retrieval},
year = {2021},
isbn = {978-3-030-92272-6},
publisher = {Springer-Verlag},
address = {Berlin, Heidelberg},
url = {https://doi.org/10.1007/978-3-030-92273-3_18},
doi = {10.1007/978-3-030-92273-3_18},
booktitle = {Neural Information Processing: 28th International Conference, ICONIP 2021, Sanur, Bali, Indonesia, December 8–12, 2021, Proceedings, Part IV},
pages = {212–223},
numpages = {12},
keywords = {Fashion retrieval, Deep learning in fashion, Centroid triplet loss, Clothes retrieval, Person re-identification},
location = {Sanur, Bali, Indonesia}
}
```

</details>


#### 2022 - Takeuchi et al - [Unsupervised Domain-Adaptive Person Re-Identification with Multi-Camera Constraints](https://arxiv.org/abs/2210.13999)

Work on reducing the loss in performance incurred when using a model in a different environment from training. 
Their method, ECA-Net, is meant for environments with overlapping camera views.
The model uses two image datasets: the source domain data (with person ID labels) and target domain data that contains only person-pair data obtained through overlapping cameras.
A CNN is used to extract features from an image, and the Jaccard distance is used to compare two persons.
The model can be trained using triplet loss on the source dataset, and identity loss on the Jaccard distance for pairs in the target domain. 

<details>
<summary>Bibtex</summary>
  
```
@INPROCEEDINGS{TakeuchiUDAReID2022,
  author={Takeuchi, Shun and Li, Fei and Iwasaki, Sho and Ning, Jiaqi and Suzuki, Genta},
  booktitle={2022 IEEE International Conference on Image Processing (ICIP)}, 
  title={Unsupervised Domain-Adaptive Person Re-Identification with Multi-Camera Constraints}, 
  year={2022},
  volume={},
  number={},
  pages={1636-1640},
  doi={10.1109/ICIP46576.2022.9897377}}
```

</details>

