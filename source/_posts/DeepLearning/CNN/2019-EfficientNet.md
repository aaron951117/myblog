---
title: 2019-EfficientNet
top: false
cover: false
toc: true
mathjax: false
date: 2023-03-18 17:50:19
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---

EfficientNet是一种基于自动缩放和神经网络结构搜索的新型卷积神经网络，它使用了一种新的方法来自动调整网络的深度、宽度和分辨率，以提高模型的精度和效率。EfficientNet在多个图像分类任务上都取得了当前最好的性能，成为了目前最为流行的卷积神经网络之一。
这些结合了其他模型的新网络，都采用了一些新的方法和思想，以提高模型的性能和效率，得到了广泛的应用。
EfficientNet是一种高效的神经网络架构，由Google Brain团队在2019年提出。它通过在不同的网络深度、宽度和分辨率下进行组合来提高性能，同时保持计算和参数的效率。

EfficientNet的基本架构是MobileNetV2，但加入了一种新的方法，即利用复合缩放系数（compound scaling）来控制模型的深度、宽度和分辨率。这个方法使用一个复合系数来缩放网络的深度、宽度和分辨率，从而得到一个更加高效的网络架构。同时，EfficientNet还使用了一种新的深度和宽度的自动化调整方法，可以根据硬件资源来选择最优的网络结构。

EfficientNet在多个图像分类、目标检测和分割任务中都取得了很好的性能表现，并且在计算和参数效率方面具有明显优势。

EfficientNet的网络框架主要由卷积层、批归一化层、激活函数和池化层构成，其中主要包括以下几个部分：
1.  卷积部分：EfficientNet采用了一种特殊的卷积操作——深度可分离卷积（Depthwise Separable Convolution），它将标准卷积拆分成两个部分，即深度卷积和逐点卷积。这种操作能够显著减少计算量，并提高模型的准确率。
2.  缩放部分：EfficientNet在卷积部分之后加入了一些缩放操作，这些操作主要包括Squeeze-and-Excitation模块和Swish激活函数。Squeeze-and-Excitation模块通过学习通道权重来提高模型的表达能力，而Swish激活函数则比常用的ReLU激活函数表现更好。
3.  池化部分：EfficientNet采用了一种自适应池化操作——Global Average Pooling（GAP），它能够将输入张量的每个通道的所有元素求平均，并输出一个张量。GAP能够减少模型的参数数量和计算量，同时还能够提高模型的泛化能力。
4.  全连接部分：EfficientNet采用了一些全连接层来将卷积部分的输出转换为最终的分类结果。

总体来说，EfficientNet的框架图与其他卷积神经网络类似，但其采用了深度可分离卷积和缩放操作等特殊的技术，使得模型更加轻量级且性能更加优秀。