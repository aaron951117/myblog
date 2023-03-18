---
title: Inception-2014-2017
top: false
cover: false
toc: true
mathjax: false
date: 2023-03-18 10:42:40
author:TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---
Inception 进化

参考链接：

[https://towardsdatascience.com/a-simple-guide-to-the-versions-of-the-inception-network-7fc52b863202](https://towardsdatascience.com/a-simple-guide-to-the-versions-of-the-inception-network-7fc52b863202)

# inception-V1 2014
Inception-v1是由Google Brain团队在2014年提出的，它是一种卷积神经网络模型，采用了多个不同大小和深度的卷积核来提取特征，同时引入了1x1卷积核来控制网络的计算复杂度，以及全局平均池化层来代替全连接层，进一步降低了模型的复杂度和参数量。Inception-v1在当时取得了很好的成绩，成为了深度学习领域中非常有影响力的模型之一。

1.  因为图像的远近导致目标主体比如狗等在画面中的位置大小不同，大的卷积核擅长提取全局信息，小的卷积核擅长局部细节信息，选择合适大小的卷积核来提取主体是比较困难的，因为不同的图像有不同的角度，所以提出的解决方案是，使用不同大小的卷积核来对同一个特征图feature map 做卷积
    
2.  使用非常深的网络结构是容易过拟合的，在整个网络更新梯度时不容易
    
3.  简单的堆积大的卷积操作计算量时非常巨大的
4. 
解决方案：

1.  在同一级别上 same level 使用 multiple size 多个大小的卷积核，使滤波器 filter 更加的wider
    
2.  为了更加节省计算量，在 3*3 或者 5*5 之前添加1*1卷积
    
3.  初步卷积stem 还有 在训练过程用到的 辅助分类器
    

  

# Inception-v2 2015

Inception-v2则是在Inception-v1的基础上进行的改进，于2015年提出。它在模块的设计上采用了分支并行结构，引入了batch normalization和residual connection等技术，进一步提高了模型的性能和稳定性。同时，它也对Inception-v1中的一些问题进行了改进，例如对网络的分支结构进行了简化，对卷积核大小的选择进行了优化等。这些改进使得Inception-v2在多个任务上都取得了很好的成绩。

  

# Inception-v3 2015

Inception-v3是由Google Brain团队于2015年提出的深度学习模型，它是Inception系列模型的第三个版本。相比于Inception-v1和Inception-v2，Inception-v3在网络架构和训练方法上都有很大的改进。

Inception-v3引入了一些新的技术，例如全局平均池化层、批标准化、权重衰减等，以进一步优化模型的性能。同时，Inception-v3还使用了更深的网络结构和更小的卷积核，提高了模型的非线性表示能力和计算效率。

1.  作者注意到 辅助分类器 在训练的最后才会起到作用，在快要曲线取向饱和之前，他们的功能类似于正则化，特别是批量正则化或者dropout操作
    
2.  在不大幅改变模块的情况下改进Inception v2的可能性有待研究。
    

解决方案：

1.  添加RMSProp优化器
    
2.  因子化 7*7 的卷积
    
3.  在辅助分类器 批量正则化
    
4.  标签平滑 预防过拟合
    

  

# Inception-v4 2016

Inception-v4是基于Inception模型和ResNet模型的结合而成，其中加入了一些ResNet的思想，如残差连接和批标准化等。同时，在模型的设计中还加入了一些新的结构，如stem结构和多尺度处理等，从而进一步提高了模型的精度和计算效率。

1.  使模块更加统一。作者还注意到，有些模块过于复杂。这使我们能够通过添加更多这些统一模块来提高性能。
    

解决方案：

1.  对Inception v4的“stem”进行了修改。这里的stem是指在引入初始块之前执行的初始操作集。
    
2.  他们有三个主要的inception模块，分别命名为A、B和C（与inception v2不同，这些模块实际上分别命名为A、B和C）。它们看起来与Inception v2（或v3）版本非常相似。
    
3.  Inception v4引入了专门的“Reduction Blocks”，用于更改网格的宽度和高度。早期版本没有明确的缩减块，但功能已经实现。reduction blocks的目的是缩小图的大小(大小指的是长和宽 而不是channel)
    

  

# Inception-ResNet-v2 2016

Inception-ResNet-v2是基于Inception模型和ResNet模型的结合而成，其中加入了一些ResNet的思想，如残差连接和批标准化等。同时，在模型的设计中还加入了一些新的结构，如scale-down模块和shortcut-connection等，从而进一步提高了模型的精度和计算效率。

  

# Inception-ResNet-v1-SE 2017

Inception-ResNet-v1-SE和Inception-ResNet-v2-SE是在Inception-ResNet-v1和Inception-ResNet-v2的基础上引入Squeeze-and-Excitation(SE)模块提出的版本，可以自适应地调整通道的权重，进一步提高了模型的性能。

Inception-ResNet-v1-SE和Inception-ResNet-v2-SE是由Google Brain团队于2017年提出的。在ImageNet和CIFAR-10数据集上的实验结果表明，引入SE模块后的模型在分类和检测任务上均获得了更好的性能。

# Inception-ResNet-v2-SE 2017