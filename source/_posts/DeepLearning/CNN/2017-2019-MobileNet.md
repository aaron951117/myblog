


![The-structural-module-of-MobileNet-V1-V2.png](https://blog95.oss-cn-beijing.aliyuncs.com/CNN/The-structural-module-of-MobileNet-V1-V2.png)



# MobileNetV1-2017

于2017年提出，其主要特点是使用深度可分离卷积（Depthwise Separable Convolution），即将传统卷积分解为两个步骤：深度卷积和逐点卷积。这种方法可以减少参数数量和计算量，从而实现高效的计算。

# MobileNetV2-2018
于2018年提出，相比于MobileNet v1，MobileNet v2引入了线性瓶颈（Linear Bottlenecks）和倒残差（Inverted Residuals）等新特性。线性瓶颈可以使网络更加稳定，而倒残差可以使网络更加深层次化。

# MobileNetV3-2019
于2019年提出，主要特点是引入了可变形卷积（Deformable Convolution）和自适应计算（Adaptive Computation）。可变形卷积可以进一步提高网络的灵活性和精度，而自适应计算可以根据硬件资源和任务需求进行网络计算量的调整。

1.  可变形卷积（Deformable Convolution）：传统的卷积操作只能在规则的矩形区域内进行卷积计算，而对于非规则形状的物体或者场景，传统卷积很难获取到准确的特征。可变形卷积则可以通过学习特征映射的偏移量，使得卷积核在非规则形状的区域内进行卷积计算，从而获取更加准确的特征。MobileNetV3使用了可变形卷积来改善在不规则形状的物体或场景中的物体检测和语义分割等任务的性能。
    
2.  自适应计算（Adaptive Computation）：传统的卷积神经网络的计算量是固定的，无法根据不同输入的大小进行动态调整。MobileNetV3提出了一种自适应计算方法，根据输入图像的大小动态调整网络的计算量，从而提高了模型的计算效率。这种自适应计算方法可以在保持模型精度的同时，减少模型的计算量和参数量。

MobileNetV3是基于网络结构搜索（Neural Architecture Search，NAS）算法进行设计的。具体来说，使用了基于梯度的强化学习方法（Reinforcement Learning，RL）进行网络结构搜索，以找到最优的网络结构，同时结合了网络剪枝（Network Pruning）和其他优化技术来进一步优化网络性能和模型大小。
MobileNetV3实际上有两篇论文，分别为：
1.  Searching for MobileNetV3（ICCV2019）
2.  MobileNetV3: A Highly Efficient Large-Scale Neural Network (arXiv:1905.02244)
其中，第一篇论文主要介绍了MobileNetV3的搜索方法和实验结果，第二篇论文则是介绍MobileNetV3的网络架构和具体实现细节。两篇论文相互补充，共同构成了MobileNetV3的完整介绍。
