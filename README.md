**一、项目背景介绍**

手写数字识别的基本原理是将输入样本数字与对应的标准样本数字进行模式匹配，将具有最大类似度的样本数字作为识别结果。该技术目前发展已比较成熟，被广泛应用在各种领域。通过学习识别手写体的原理，可拓展到识别手写文字研究。

**二、数据介绍**

项目使用MNIST数据集，其含有60000个训练集和10000个测试集，主要分类图片和标签，其中图片是28*28的像素矩阵，标签是0~9折10个数字。

项目代码分别使用paddle.dataset.mnist.train()和test()获取mnist的训练集和测试集。

![](https://ai-studio-static-online.cdn.bcebos.com/f175249d5b7f4cbd823092ee4a00a2a86d591257365040ab94c2b35c9d147ea3)

**三、模型介绍**


手写体数字识别过程中，主要是通过对图片进行特征提取进行数字识别。这次实践使用多层感知器训练DNN模型，在paddle环境下编程，多层感知器结构：输入层->隐藏层->隐藏层->输出层 主要的步骤有：数据准备（构造数据提供器），网络配置（网络模型、损失函数使用交叉熵、优化函数使用Adam，学习率为0.001），模型训练（训练、保存模型）等

**四、模型训练**

    1.首先创建训练的Executor;

    2.将数据分为image和label两部分；

    3.绘制出模型曲线并将其保存

**五、模型评估**

对于灰度图片可以准确识别出图片的数字，但无法准确识别出彩色图片。因此这个模型还有待改进。

**六、个人总结**

这是我第一次学习并动手模仿完成的一个小项目，第一次使用github，由于知识学得不是很牢固，大多数代码都是对照着写然后自己再去理解。后续会不断改进并更新该项目。万事开头难，希望后面能在图像处理方向不断前进！
