
# Graph classification with muti-scenario cyber security


# Auto Graph Neural Network  Based Block Pool for muti-scenario cyber security


# IEEE搜索
1. evolution graph architecture search 结果 7
2. evolution graph architecture 结果 101
3. neural architecture search || evolutionary || 2018-2023  239
4. neural architecture search || evolution || 2018-2023 79
5. neural architecture search || 2018-2023 1851

## 创新点
1. 首次将ENAS运用到图神经网络做信息入侵识别
2. 为了让进化过程探索空间更广泛从而有更大的可能性得到符合各个目标标准的个体，种群初始化生成了所有的长度，均匀的在搜索空间选择操作。
3. 大部分的多目标神经架构演化是有精度和其他指标是硬件消耗限制方面，比如内存占用，模型参数量，flops等。而我们的目标与大多数工作不同。我们的目标仍然是考虑模型的指标。具体来说，f1分数，主要是查准率，尽可能找出的入侵报文或者程序是被正确分类的。and 召回率，尽可能把正常报文或者程序的入侵部分找出来避免遗漏。在保证查准率和查全率的基础上，我们还引入了评价模型性能好坏的指标ROC值。因为我们所应用的部署的场景不同，侧重方面不同，可以选取符合应用场景并且适合部署网络硬件资源的神经网络个体。网络安全有多种应用场景，并且不同的应用场景的侧重点不同。比如工业的网络安全着重于把尽可能值得怀疑的信息片段都捕捉到，在实时性高的应用场景，更需要是捕捉真正的入侵信息，以免在系统工作中频繁的触发防护机制，比如车辆网络安全。


## 前导知识
https://xie.infoq.cn/article/1fce9a0462909bcf1604db9b0
1. Cyber Security is a branch of information security that deals with preserving internet-connected devices, such as devices, operating systems, programs, and data, from potential cyberattacks. cyber security网络安全是信息安全的一个分支，负责保护物联网设备（例如设备、操作系统、程序和数据）免受潜在的网络攻击。
2. 信息安全包括网络安全，信息安全还包括操作系统安全，数据库安全，硬件设备和设施安全，物理安全，人员安全，软件开发，应用安全等。
3.   网络安全更注重在网络层面，例如通过部署防火墙、入侵检测等硬件设备来实现<mark>链路层面</mark>的安全防护，而信息安全的层面要比网络安全的覆盖面大的多，信息安全是从<mark>数据</mark>的角度来看安全防护。通常采用的手段包括：防火墙、入侵检测、审计、渗透测试、风险评估等，安全防护不仅仅是在网络层面，更加关注的应用层面，可以说信息安全更贴近于用户的实际需求及想法。

## 应用主题
1. 网络安全（Cyber Security），指得是检测网络（链路）受到外部入侵的情况。


## 学位论文创新点
1. 因此使用众所周知的帕累托优势 (PD) 概念来确定哪个个体更好。如果满足以下条件之一，则称一个人支配另一个人：（1）它具有更高的分类精度， 以及更少或相等数量的可训练参数，或（2）它具有更高或相等的分类准确性，以及较少数量的可训练参数。对于每个个体，支配它的个体都被计算在内。受其支配的个体数量越少的个体被视为越好。（支配我的个体越少，则确定解的质量越好）