# Video Scene Graph Generation

#### 2023 - Yang et al. - [Panoptic Video Scene Graph Generation](https://openaccess.thecvf.com/content/CVPR2023/papers/Yang_Panoptic_Video_Scene_Graph_Generation_CVPR_2023_paper.pdf)

[Official Pytorch implementation](https://github.com/LilyDaytoy/OpenPVSG)

Towards building comprehensive real-world visual perception systems, we propose and study a new problem called panoptic scene graph generation (PVSG). 
PVSG is related to the existing video scene graph generation (VidSGG) problem, which focuses on temporal interactions between humans and objects localized with bounding boxes in videos.
However, the limitation of bounding boxes in detecting non-rigid objects and backgrounds often causes VidSGG systems to miss key details that are crucial for comprehensive video understanding.
In contrast, PVSG requires nodes in scene graphs to be grounded by more precise, pixel-level segmentation masks, which facilitate holistic scene understanding.
To advance research in this new area, we contribute a high-quality PVSG dataset, which consists of 400 videos (289 third-person + 111 egocentric videos) with totally 150K frames labeled with panoptic segmentation masks as well as fine, temporal scene graphs. 
We also provide a variety of baseline methods and share useful design practices for future work.

<details>
<summary>Bibtex</summary>
 
```
@inproceedings{yang2023pvsg,
    author = {Yang, Jingkang and Peng, Wenxuan and Li, Xiangtai and Guo, Zujin and Chen, Liangyu and Li, Bo and Ma, Zheng and Zhou, Kaiyang and Zhang, Wayne and Loy, Chen Change and Liu, Ziwei},
    title = {Panoptic Video Scene Graph Generation},
    booktitle = {CVPR},
    year = {2023},
}
```

</details>


#### 2024 - Wang et al. - [Taking a Closer Look At Visual Relation: Unbiased Video Scene Graph Generation With Decoupled Label Learning](https://arxiv.org/abs/2303.13209v1)

Current video-based scene graph generation (VidSGG) methods have been found to perform poorly on predicting predicates that are less represented due to the inherent biased distribution in the training data. 
In this paper, we take a closer look at the predicates and identify that most visual relations (e.g. sit_above) involve both actional pattern (sit) and spatial pattern (above), while the distribution bias is much less severe at the pattern level. 
Based on this insight, we propose a decoupled label learning (DLL) paradigm to address the intractable visual relation prediction from the pattern-level perspective. 
Specifically, DLL decouples the predicate labels and adopts separate classifiers to learn actional and spatial patterns respectively. The patterns are then combined and mapped back to the predicate. 
Moreover, we propose a knowledge-level label decoupling method to transfer non-target knowledge from head predicates to tail predicates within the same pattern to calibrate the distribution of tail classes.

<details>
<summary>Bibtex</summary>
 
```
@article{DBLP:journals/tmm/WangLCJYX24,
  author       = {Wenqing Wang and
                  Yawei Luo and
                  Zhiqing Chen and
                  Tao Jiang and
                  Yi Yang and
                  Jun Xiao},
  title        = {Taking a Closer Look At Visual Relation: Unbiased Video Scene Graph
                  Generation With Decoupled Label Learning},
  journal      = {{IEEE} Trans. Multim.},
  volume       = {26},
  pages        = {5718--5728},
  year         = {2024},
  url          = {https://doi.org/10.1109/TMM.2023.3338078},
  doi          = {10.1109/TMM.2023.3338078},
  timestamp    = {Mon, 15 Apr 2024 08:25:39 +0200},
  biburl       = {https://dblp.org/rec/journals/tmm/WangLCJYX24.bib},
  bibsource    = {dblp computer science bibliography, https://dblp.org}
}
```

</details>
