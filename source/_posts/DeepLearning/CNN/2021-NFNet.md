---
title: ResNet-2
top: false
cover: false
toc: true
mathjax: false
date: 2023-03-18 10:46:53
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
NFNet（Normalizer-Free Networks）是由谷歌研究团队于2021年提出的一种深度卷积神经网络结构。与传统的神经网络不同，NFNet不需要使用批标准化（Batch Normalization）等归一化方法，而是使用通道注意力机制和动态卷积核来增强模型的表示能力和泛化能力。

NFNet的设计思想源于对批标准化的一些限制和缺陷的探索和反思，如对小批量数据的处理不稳定、在训练和测试阶段的差异性、对噪声和抖动数据的敏感性等。NFNet使用了一些新的技术和策略，如通道注意力机制、自适应梯度裁剪、动态卷积核等，以改善模型的性能和泛化能力。

NFNet在ImageNet分类任务上的表现非常出色，超过了当时的SOTA模型，并且在大量图像分类、目标检测和语义分割任务中都达到了最佳效果。NFNet的提出对于深度学习领域的发展和实践具有重要的意义。

NFNet一共提出了两个版本：NFNet-F1和NFNet-F2。这两个版本的网络结构相似，但在一些细节上有所不同。