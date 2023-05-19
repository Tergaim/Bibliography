# Computer Vision

Computer Vision encompasses any task that involves the processing and analysis of image and video data.
This page is for generic papers that can be applied to multiple fields of computer vision; see the other pages for specialized tasks.

#### 2016 - He et al. - [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)

Introduce the ResNet architecture. Instead of simply stacking layers, they introduce residual blocks that, for an input x, output F(x)+x. 
Adding the input to the block result effectively create shortcut connections that greatly reduce or eliminate training problems (vanishing gradient, accuracy degradation) that can occur in stacked layers.
This allows for easy accuracy gains by simply stacking more residual blocks, often with a lower computational complexity than contemporary SOTA while significantly outperforming it.

#### 2020 - Cordonnier et al. - [On the relationship between Self-Attention and Convolutonal Layers](https://arxiv.org/abs/1911.03584)

[Official Pytorch implementation](https://github.com/epfml/attention-cnn)

In this work, the authors put forth theoretical and empirical evidence that self-attention layers learn to behave similar to convolutional layers:
1. From a theoretical perspective, they provide a constructive proof showing that self-attention layers can express any convolutional layers.
Specifically, they show that a single multi-head self-attention layer using relative positional encoding can be re-parametrized to express any convolutional layer.
2. Their experiments show that the first few layers of attention-only architectures do learn to attend on grid-like pattern around each query pixel, similar to the theoretical construction.

#### 2021 - Dosovitskiy et al. - [An Image is Worth 16x16 Words: Transformers fo Image Recognition at Scale](https://arxiv.org/abs/2010.11929)

[Official Tensorflow implementation](https://github.com/google-research/vision_transformer)

Aim at showing that Vision Transformer (ViT) can be applied to image recognition while completely eliminating convolution layers.
They split images into patches similar to NLP word tokens. While this approach is outperformed by CNNs on small datasets, it achieves better results when pre-trained on large datasets and fine-tuned for specific applications.
Compared to Cordonnier 2020, use bigger patch size which allows for handling higher resolution images. They follow the original transformer architecture (Vaswani 2017) as much as possible.
When fine-tuning, the classification head is replaced by a new classification layer. Additionally, the authors recommend fine-tuning at a higher resolution than pre-training.
The architecture itself allows for input data of arbitrary size, but positional information in token should be interpolated to reflect pretraining position embeddings.
