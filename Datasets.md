# Datasets

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

## Person Re-Identification

#### Market 1501

2015 - Zheng et al - [Scalable Person Re-identification: A Benchmark](https://www.cv-foundation.org/openaccess/content_iccv_2015/papers/Zheng_Scalable_Person_Re-Identification_ICCV_2015_paper.pdf)

[Downlodable from here](https://zheng-lab.cecs.anu.edu.au/Project/project_reid.html)
