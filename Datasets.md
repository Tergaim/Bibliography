# Datasets

## Action Recognition

#### NTU RGB+D

2016 - Shahroudi et al. - [NTU RGB+D: A Large Scale Dataset for 3D Human Activity Analysis](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Shahroudy_NTU_RGBD_A_CVPR_2016_paper.pdf)

2020 - Liu et al. - [NTU RGB+D 120: A Large-Scale Benchmark for 3D Human Activity Understanding](https://arxiv.org/abs/1905.04757)

[Instructions for download](https://github.com/shahroudy/NTURGB-D) 

Set of actions each containing RGB videos, sequences of depth maps, 3D skeletal data and infrared videos. The original version contains 60 actions, extended to 120 in 2020.
The 2020 version is also made for one-shot action recognition.

## Human-Object Interaction

#### HICO-DET

2018 - Chao et al. - [Learning to Detect Human-Object Interactions](https://arxiv.org/abs/1702.05448)

[Official Caffe implementation](https://github.com/ywchao/ho-rcnn)

[Downloadable from here](http://websites.umich.edu/~ywchao/hico/)

Introduce HICO-DET benchmark:  150k images with bounding boxes for human, object, and interaction type (600 interaction categories).
Each interaction type includes action and objects (eg., "riding a bike", "eating an apple"...)

#### V-COCO

2015 - Gupta and Malik - [Visual Semantic Role Labeling](https://arxiv.org/abs/1505.04474)

[Instructions for download here](https://github.com/s-gupta/v-coco)

Dataset of 10k images (16k people) doing 26 different actions (verbs), based on captioned images from the COCO dataset.
Actions include interactions with 0 to 2 objects. Bounding boxes are provided for the human and objects.
Two tasks are associated with this dataset:
1. Agent detection (find the person executing a particular action), measured by precision.
2. Role detection (find human and objects associated with an action), measured by bouding box overlap.

## Object Detection

#### COCO

2014 - Lin et al - [Microsoft COCO: Common Objects in Context](https://arxiv.org/abs/1405.0312)

[Download here](https://cocodataset.org/#download)

Dataset of 1.5m objet instances over 118k images. Originally released in 2014, but slight modifications (including different train/test splits) in the following years.
Includes 80 object categories; each individual object instance is segmented, with multiple objects (sometimes multiple instanes of the same object) per image.
The dataset has been expanded with people segmentation and keypoints. 
Used for multiple tsk, including reoccurring challenges:
1. Object detection (segmentation)
2. Keypoint detection
3. Image segmentation (objects and "stuff" like sky, road...)
4. Captioning

#### FashionStyle14

2017 - Takagi et al - What Makes a Style: Experimental Analysis of Fashion Prediction [(IEEE)](https://ieeexplore.ieee.org/document/8265473) 

[Download here](https://esslab.jp/~ess/en/data/fashionstyle14/)

New dataset for fashion style prediction, which consists of 14 different fashion styles each with roughly 1,000 images of worn outfits. 
The dataset, with a total of 13,126 images, captures the diversity and complexity of modern fashion styles. 
The paper benchmarks a wide variety of modern classification networks, and also perform an in-depth user study with both fashion-savvy and fashion-naïve users. 
Although classification networks are able to outperform naive users, they are still far from the performance of savvy users.
The download link also leads to bigger datasets on the same topic. 

## Person Re-Identification

#### Market 1501

2015 - Zheng et al - [Scalable Person Re-identification: A Benchmark](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Zheng_Scalable_Person_Re-Identification_ICCV_2015_paper.pdf)

[Downlodable from here](https://zheng-lab.cecs.anu.edu.au/Project/project_reid.html)

## Distribution Shifts

#### WILDS

2020 - Koh et al. - [WILDS: A Benchmark of in-the-Wild Distribution Shifts](https://arxiv.org/abs/2012.07421)

[Downloadable from here](https://wilds.stanford.edu/)

Collection of 10 datasets selected to cover scenarios with various ranges of distribution shifts, which standard methods struggle to learn.

## Video Scene Graph Generation

#### STAR

2021 - Wu et al. - [STAR: A Benchmark for Situated Reasoning in Real-World Videos](https://openreview.net/pdf?id=EfgNF5-ZAjM)

[Downloadable from here](https://bobbywu.com/STAR/#repo)

The dataset consists of four question types for situated reasoning: Interaction, Sequence, Prediction, and Feasibility. Video situations are decomposed by bottom-up hyper-graphs with atomic entities and relations (e. g., actions, objects, and relationships).

#### VidVRD

2017 - Shang et al. - [Video Visual Relation Detection](https://www-users.cse.umn.edu/~guo00109/assets/publication/mm17-shangxd.pdf)

[Downloadable from here](https://xdshang.github.io/docs/imagenet-vidvrd.html) 

The dataset contains 1,000 videos selected from ILVSRC2016-VID dataset based on whether the video contains clear visual relations. It is split into 800 training set and 200 test set, and covers common subject/objects of 35 categories and predicates of 132 categories.
