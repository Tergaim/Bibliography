#### 2018 - Chao et al. - [Learning to Detect Human-Object Interactions](https://arxiv.org/abs/1702.05448)

[Official Caffe implementation](https://github.com/ywchao/ho-rcnn) \
[Dataset available here](http://websites.umich.edu/~ywchao/hico/)

Introduce HICO-DET benchmark:  150k images with bounding box for human, object, and interaction type (600 interaction categories).
Each interaction type includes action and objects (eg., "riding a bike", "eating an apple"...)
Propose a model that works in two parts:
1. Detects human/object bounding boxes. Uses one detector per object in the list of interactions.
2. Uses DNN on each box and on the union to classify the interaction.

#### 2021 - Zhang et al. - [Mining the Benefits of Two-stage and One-stage HOI Detection](https://arxiv.org/abs/2108.05077)

[Official Pytorch implementation](https://github.com/YueLiao/CDN)

Compares benefits and drawbacks of 2-stage (HO detection and I classification) vs 1-stage HOI methods.
2-stage : additional time complexity, potential lack of context in 2nd stage, lots of negative samples. However specialized models are good at each stage.
1-stage : direct focus on interaction point, but difficult to find good feature representation for both tasks.
Introduce CDN, 1-stage model that works in 3 steps (cascade decoders): visual features extraction, human/object detection, interaction classification.

#### 2023 - Guo et al. - [Body Part Information Additional in Multi-decoder Transformer-Based Network for Human Object Interaction Detection](https://www.scitepress.org/PublishedPapers/2023/117553/)

Multi-decoder structure: Detects object and human bounding box, then body part, then classifies interaction. Similar to CDN (Zhang 2021) with added body part module.
Focus on the hand with 50 verbs from the HICO DET (Chao 2018) dataset.
