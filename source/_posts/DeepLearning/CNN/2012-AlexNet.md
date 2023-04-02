---
title: 2012-AlexNet
top: false
cover: false
toc: true
mathjax: false
date: 2022-02-04 10:47:01
author: TianShan
img:
coverImg:
password:
summary:
tags:
categories:
---

AlexNet网络结构共有8层，其中有5个卷积层和3个全连接层。其网络结构如下

![alexnet.png](https://blog95.oss-cn-beijing.aliyuncs.com/CNN/alexnet.png)


AlexNet是在2012年由Alex Krizhevsky等人提出的深度神经网络模型，是ImageNet挑战赛2012年的冠军模型。其具有以下特点：

1.  使用了ReLU激活函数代替sigmoid，使得神经网络训练速度加快；
2.  使用了Dropout技术防止过拟合；
3.  使用了数据增强技术增加数据量；
4.  使用了GPU进行训练加速。



# 李沐

- ImageNet是当时图片分类最大的数据集
- 在当时机器学习界很小，看到作者大概就可以判断出科研风格
- 这篇论文虽然发表在机器学习最好的会议，但是主要的影响一开始在计算机视觉界，毕竟ImageNet是计算机视觉的数据集
- 计算机视觉对刷榜比较在意，在意是否有效，所以对于理论的完整性不是很感冒，随着研究的人慢慢增多，从而扩展到其他地方
- NVIDIA在2007年出了cuda库，在2012年使用GPU算比较正常，在2012年之后，GPU在机器学习界使用较多
- 文章没有结论，讨论更多是吐吐槽，和未来要干什么，结论一般是和摘要的一一对应，没有结论少见