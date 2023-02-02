
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

