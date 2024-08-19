# YOLO介绍
-------------------
**参考资料：** 
- [yolo原理详解](https://blog.csdn.net/DFCED/article/details/105157452)
- [一文弄懂yolo算法](https://developer.aliyun.com/article/679591)
- [卷积神经网络原理](https://poloclub.github.io/cnn-explainer/)
- [什么是神经网络](https://www.ibm.com/cn-zh/topics/neural-networks)
- [DNN原理](https://blog.csdn.net/myTomorrow_better/article/details/138817202)
。
## 一、什么是神经网络
### 1. 神经网络
神经网络可分为不同类型，用于不同的目的。
感知器是最古老的神经网络，由 Frank Rosenblatt 在 1958 年创建。

前馈神经网络或多层感知器 (MLP) 。它们由一个输入层、一个或多个隐藏层和一个输出层组成。虽然这些神经网络通常也被称为 MLP，但它们实际上由 sigmoid 神经元而不是感知器组成，因为大多数现实世界的问题都是非线性的。数据通常被输入到这些模型中进行训练，它们是计算机视觉、自然语言处理和其他神经网络的基础。

卷积神经网络 (CNN) 与前馈网络类似，但它们通常用于图像识别、模式识别和/或计算机视觉。这些网络利用线性代数，尤其是矩阵乘法的原理来识别图像中的模式。

循环神经网络 (RNN) 可通过其反馈循环来识别。这些学习算法主要用于使用时间序列数据对未来结果进行预测，例如股票市场预测或销售预测。
### 2. 深度神经网络
一个由超过三层（包括输入层和输出层）构成的神经网络可以被视为一个深度神经网络 (DNN) 。只有两层或三层的神经网络只是一个基本的神经网络。

## 二、什么是YOLO
YOLO，全称为“You Only Look Once”（你只需看一次），是一种流行的实时目标检测算法。它由Joseph Redmon等人于2015年首次提出，并且随着时间发展，已经推出了多个版本，如YOLOv2、YOLOv3、YOLOv4、**YOLOv5**、**YOLOv8**等
## 三、特点

快速：YOLO算法能够在单次前向传播中同时预测多个边界框和类别概率，因此检测速度快，适合实时应用。

整体性：与传统的目标检测算法不同，YOLO将目标检测问题视为一个回归问题，直接从图像像素到边界框坐标和类别概率的映射，而不是使用滑动窗口或区域建议网络。

端到端：YOLO算法是端到端的，即从输入图像到输出检测结果的整个过程是连续的，不需要额外的后处理步骤。

多尺度检测：YOLO能够检测不同尺寸的目标，因为它在多个尺度上进行预测。

基于深度学习：YOLO算法通常使用深度卷积神经网络（如Darknet）作为其特征提取器。

## 四、基本原理
yolo将输入图像划分为一个个格子（grid cell），每个格子负责预测该格子中心点为中心的边界框和类别概率。每个格子会预测多个边界框，每个边界框包括边界框的位置（x, y, width, height）和对象存在的置信度（confidence score），以及边界框内可能的类别概率。
**置信度**：主要取决于两个方面，框内存在目标的概率和该目标是某一类的概率

## 五、使用场景

[车辆识别和测距](https://www.bilibili.com/video/BV1tR4y1P7sN/?spm_id_from=333.337.search-card.all.click&vd_source=eeb6cc78f675673877f3c068e8ef394c)
[体育竞赛](https://www.bilibili.com/video/BV1ct4y1E7Gp/?spm_id_from=333.337.search-card.all.click&vd_source=eeb6cc78f675673877f3c068e8ef394c)
[ROBOCON2023吴哥之花](https://www.bilibili.com/video/BV1124y1M7EG/?spm_id_from=333.337.search-card.all.click&vd_source=eeb6cc78f675673877f3c068e8ef394c)
[RM能量符识别](https://www.bilibili.com/video/BV1bL411X7UQ/?spm_id_from=333.788.recommend_more_video.3&vd_source=eeb6cc78f675673877f3c068e8ef394c)
...