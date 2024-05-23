# Scene Graph Generation

#### 2023 - Li et al. - [Zero-Shot Scene Graph Generation via Triplet Calibration and Reduction](https://arxiv.org/abs/2309.03542)

[Official Pytorch implementation](https://github.com/jkli1998/T-CAR)

Existing SGG methods typically suffer from poor compositional generalizations on unseen triplets. 
They are generally trained on incompletely annotated scene graphs that contain dominant triplets and tend to bias toward these seen triplets during inference. 
To address this issue, we propose a Triplet Calibration and Reduction (T-CAR) framework in this paper. 
In our framework, a triplet calibration loss is first presented to regularize the representations of diverse triplets and to simultaneously excavate the unseen triplets in incompletely annotated training scene graphs. 
Moreover, the unseen space of scene graphs is usually several times larger than the seen space since it contains a huge number of unrealistic compositions. 
Thus, we propose an unseen space reduction loss to shift the attention of excavation to reasonable unseen compositions to facilitate the model training. 
Finally, we propose a contextual encoder to improve the compositional generalizations of unseen triplets by explicitly modeling the relative spatial relations between subjects and objects. 

<details>
<summary>Bibtex</summary>
 
```
@article{li2023zero,
  title={Zero-Shot Scene Graph Generation via Triplet Calibration and Reduction},
  author={Li, Jiankai and Wang, Yunhong and Li, Weixin},
  journal={ACM Transactions on Multimedia Computing, Communications and Applications},
  year={2023},
  publisher={ACM New York, NY}
}
```

</details>

#### 2023 - Zhao and Xu - [Less is More: Toward Zero-Shot Local Scene Graph Generation via Foundation Models](https://arxiv.org/abs/2310.01356)

Humans inherently recognize objects via selective visual perception, transform specific regions from the visual field into structured symbolic knowledge, 
and reason their relationships among regions based on the allocation of limited attention resources in line with humans' goals. 
While it is intuitive for humans, contemporary perception systems falter in extracting structural information due to the intricate cognitive abilities and commonsense knowledge required. 
To fill this gap, we present a new task called Local Scene Graph Generation. 
Distinct from the conventional scene graph generation task, which encompasses generating all objects and relationships in an image, our proposed task aims to abstract pertinent structural information with partial objects and their relationships for boosting downstream tasks that demand advanced comprehension and reasoning capabilities. 
Correspondingly, we introduce zEro-shot Local scEne GrAph geNeraTion (ELEGANT), a framework harnessing foundation models renowned for their powerful perception and commonsense reasoning, where collaboration and information communication among foundation models yield superior outcomes and realize zero-shot local scene graph generation without requiring labeled supervision. 
Furthermore, we propose a novel open-ended evaluation metric, Entity-level CLIPScorE (ECLIPSE), surpassing previous closed-set evaluation metrics by transcending their limited label space, offering a broader assessment. 

<details>
<summary>Bibtex</summary>
 
```
@misc{zhao2023more,
      title={Less is More: Toward Zero-Shot Local Scene Graph Generation via Foundation Models}, 
      author={Shu Zhao and Huijuan Xu},
      year={2023},
      eprint={2310.01356},
      archivePrefix={arXiv},
      primaryClass={cs.CV}
}
```

</details>
