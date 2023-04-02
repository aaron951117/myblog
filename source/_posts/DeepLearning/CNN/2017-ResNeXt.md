---
title: 2017-ResNeXt
top: false
cover: false
toc: true
mathjax: false
date: 2023-03-18 17:50:11
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---

ResNeXt是由微软亚洲研究院提出的深度残差网络（ResNet）的改进版，是一种基于多分支卷积神经网络的深度学习模型。ResNeXt通过在每个残差块中使用一组并行的卷积分支来增加网络的宽度，从而提高了模型的性能。与ResNet的单一分支相比，ResNeXt具有更少的参数，更好的精度和更高的计算效率。

ResNeXt的核心思想是使用一组基本块的组合来构建网络结构，这些基本块具有相同的拓扑结构，但具有不同的权重。这些基本块中的每一个都由多个并行的分支组成，每个分支都是一个卷积神经网络，然后将所有分支的输出合并在一起。这种设计使得ResNeXt可以通过增加并行的分支来增加网络的宽度，而不是增加深度或参数数量。

ResNeXt的设计思想使得它在多个计算机视觉任务上都取得了优异的性能表现，如图像分类、目标检测和语义分割等



![ResNeXt.png](https://blog95.oss-cn-beijing.aliyuncs.com/CNN/ResNeXt.png)

```scss
Input
 |
 |--Convolutional layer (64 filters, 7x7, stride=2)
 |   |--Batch Normalization
 |   |--ReLU
 |
 |--Max pooling (3x3, stride=2)
 |
 |--Block 1 (4x)
 |   |--Split-transform-merge (256 filters, 1x1)
 |   |--Split-transform-merge (256 filters, 3x3)
 |   |--Split-transform-merge (256 filters, 1x1)
 |
 |--Block 2 (4x)
 |   |--Split-transform-merge (512 filters, 1x1)
 |   |--Split-transform-merge (512 filters, 3x3)
 |   |--Split-transform-merge (512 filters, 1x1)
 |
 |--Block 3 (4x)
 |   |--Split-transform-merge (1024 filters, 1x1)
 |   |--Split-transform-merge (1024 filters, 3x3)
 |   |--Split-transform-merge (1024 filters, 1x1)
 |
 |--Block 4 (4x)
 |   |--Split-transform-merge (2048 filters, 1x1)
 |   |--Split-transform-merge (2048 filters, 3x3)
 |   |--Split-transform-merge (2048 filters, 1x1)
 |
 |--Average pooling (7x7)
 |
 |--Fully connected layer (1000 units)
 |
Output
```
