# Deep Learning Papers
* [conditional-generative-adversarial-networks](#conditional-generative-adversarial-networks)
* [Batch_Normalization](#batch-normalization-accelerating-deep-network-training-by-reducing-internal-covariate-shift)
* [Batch_renormalization](#batch-renormalization-towards-reducing-minibatch-dependence-in-batch-normalized-models)

### [conditional generative adversarial networks](https://github.com/JulyEdu-PaperTranslation/DeepLearning/blob/master/conditional_generative_adversarial_networks/CGAN%E7%BF%BB%E8%AF%91.pdf)
* **题目**: 条件生成对抗网络
* **翻译**:张兴园 (初), 路转(复), 管枫(审)
* **绪论**：[**生成式对抗网络(GAN)**](https://arxiv.org/pdf/1406.2661.pdf)是一种用来训练生成式模型的新方法。本文中，我们在GAN的基础之上引入条件生成式对抗网络，它的构建并不复杂，只需要在生成模型与判别模型的构建中分别输入条件数据y。实验结果显示此模型能够在类别标签条件下生成MNIST手写体数字。对于多模态模型的训练，本文也给出了一个生成图像标记的初步示例，我们在这个示例中展示如何生成训练标签之外的描述性标签。
* **译者注**：条件生成对抗网络的原理比较简单，只需要在生成器和判别器中分别输入相同的条件变量，但是却可以有效地引导模型的数据生成。本文介绍了条件生成对抗网络的原理以及两个应用，结构如下：
 * (1) 简介
 * (2) 相关工作
 * (3) 条件生成对抗网络原理
 * (4) 应用  
    1. 单模态：生成手写体数字  
    2. 多模态: 生成图片文字标注
* **翻译全文下载**:[pdf](https://github.com/JulyEdu-PaperTranslation/DeepLearning/blob/master/conditional_generative_adversarial_networks/CGAN%E7%BF%BB%E8%AF%91.pdf)

**[更多文章](#deep-learning-papers)**

### [Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift](https://github.com/JulyEdu-PaperTranslation/DeepLearning/blob/master/Batch_Normalization/arx.pdf)
* **题目**: 批量规范化：通过减少内部协变量转移加速深度网络训练
* **翻译**：陈媛媛(初)，管枫(复)，任远航(审)
* **绪论**：在深度神经网络的训练过程中，先前层参数的调整会导致之后每一层输入值的分布发生变化，这种现象使模型的训练变得很复杂。所以在深度神经网络模型的训练中，通常需要仔细选取初始参数并采取较小的学习率，这不但导致模型训练的效率低下，而且使得饱和非线性模型的训练极为困难。我们把这种现象称为内部协变量转移(covariate shift)，并通过规范化(normalizing)每层的输入来解决这个问题。我们方法的强大之处在于把规范化的步骤作为模型训练架构的一部分来实现, 并且对每个训练小批量都执行规范化操作。批量规范化允许我们使用很高的学习率并且对初始化不太在意。它在一定情况下也可以起到正则化的作用，并减轻了对Dropout的需求。我们在最先进的图像分类模型中使用批量规范化法，在减少了14倍训练步骤的情况下实现了与原模型相同的精度，并以显著增量击败了原始模型。我们使用批量规范化的网络模型，增强了在ImageNet分类上发布的最佳结果:获得了4.9%前5验证误差（和4.8%测试误差），这超出了人类评估者的准确率。
* **译者注**：本文将原本对于整个训练网络定义的协变量转移这个概念推广到了训练网络中任何一个层或者子网络，称之为内部协变量转移。文中提出了使用规范化的方法来减少内部协变量转移，而批量规范化使得文中提到的规范化可以与常用的批量梯度下降法相协调。简单来说，批量规范化使得深层网络中每一层的输入都得到了一定程度的规范化，这使得每一层的训练都更加快速和稳定，从而改善了整体网络训练的效率与精度。
 * **文章结构:**
 * (1) 简介: 提出内部协变量转移的动机
 * (2) 如何减少内部协变量转移
 * (3) 批量规范化法在深度学习网络中算法实现
 * (4) 实验结果
 * (5) 结论与展望
* **翻译全文下载**:([pdf](https://github.com/JulyEdu-PaperTranslation/DeepLearning/blob/master/Batch_Normalization/arx.pdf),[word](https://github.com/JulyEdu-PaperTranslation/DeepLearning/blob/master/Batch_Normalization/%E7%BF%BB%E8%AF%91%E7%A8%BFWORD%E7%89%88.docx))

**[更多文章](#deep-learning-papers)**


### [Batch Renormalization: Towards Reducing Minibatch Dependence in Batch-Normalized Models](https://github.com/JulyEdu-PaperTranslation/DeepLearning/tree/master/Batch_remormalization)
* **题目**: 批再规范化：减少批量规范化模型对小批量的依赖
* **翻译**：smile(初)，管枫(复)，seed(审)
* **绪论**：批规范化可以十分有效地加速和提升深度模型的训练。但是，当训练的 minibatch 较小或不是由独立的样本组成时，它的有效性会降低。我们假设这主要归因于如下两点，一是minibatch里样本的层输入之间有相关性，二是模型的训练和推理中输出的激活不同。我们提出了一种简单有效的扩展——批再规范化，以确保训练和推理模型可以输出相同的激活，而且这个输出是基于单个样本而非整个 minibatch。当训练时的minibatch比较小或者non-i.i.d.（非独立同分布）时，用批再规范化训练的模型表现显著优于批规范化训练的模型。与此同时，批再规范化还保留了批规范化的优点，例如对初始化的不敏感和高训练效率。
* **译者注**：批规范化试图使用minibatch的均值和方差对自己进行规范化，这种做法的有效性立足于minibatch的均值和方差可以代表整体训练集的均值和方差。所以当minibatch很小或者内部存在较强的相关性时，批规范化的效果就会受到影响。批再规范化在训练过程中逐步估计整体训练集的层输出的期望及方差,并以此来进行规范化操作。这种做法避免了每一个minibatch用自己的期望方差来规范自己的这种窘境，从而显著提高了小minibatch与非独立同分布minibatch情形下的训练效果。
 * **文章结构:**
 * (1) 简介: 提出研究批再规范化的动机
 * (2) 回顾批规范化
 * (3) 介绍批再规范化的原理与实现
 * (4) 实验结果
 * (5) 结论与展望
* **翻译全文下载**:([pdf](https://github.com/JulyEdu-PaperTranslation/DeepLearning/tree/master/Batch_remormalization/arxiv.pdf))

**[更多文章](#deep-learning-papers)**

### [An overview of gradient descent optimization algorithms](https://github.com/JulyEdu-PaperTranslation/DeepLearning/tree/master/AnOverviewOfGradientDescentOptimizationAlgorithms)
* **题目**: 
* **翻译**：彭博(初)，管枫(复)，(审)
* **绪论**：
* **译者注**：
 * **文章结构:**
 * (1) 
 * (2) 
 * (3) 
* **翻译全文下载**:()

