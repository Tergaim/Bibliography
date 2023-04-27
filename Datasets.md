## Human-Object Interaction

**HICO-DET**
2018 - Chao et al. - [Learning to Detect Human-Object Interactions](https://arxiv.org/abs/1702.05448)
[Official Caffe implementation](https://github.com/ywchao/ho-rcnn)
[Dataset available here](http://websites.umich.edu/~ywchao/hico/)
Introduce HICO-DET benchmark:  150k images with bounding box for human, object, and interaction type (600 interaction categories).
Each interaction type includes action and objects (eg., "riding a bike", "eating an apple"...)
Propose a model that works in two parts:
1. Detects human/object bounding boxes. Uses one detector per object in the list of interactions.
2. Uses DNN on each box and on the union to classify the interaction.


## TO SORT

**V-COCO**
2015 - - [Visual Semantic Role Labeling](https://arxiv.org/abs/1505.04474)
