# Deep Learning Papers
* [conditional_generative_adversarial_networks](#conditional_generative_adversarial_networks)
* [Batch_Normalization](#Batch_Normalization)

### conditional_generative_adversarial_networks
* Title:Conditional Generative Adversarial Networks
* 翻译:张兴园 (初),路转 (复),管枫(mapleguan)(审)
* 文章下载：conditional_generative_adversarial_networks/CGAN翻译.pdf

### Batch_Normalization
* Title:Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift
* 批量归一化：通过减少内部协变量转移加速深度网络训练
* 翻译：Kenny(初)，管枫(复)，任远航(审)
* 绪论：
  在深度神经网络的训练过程中，先前层参数的调整会导致之后每一层输入值的分布发生变化，这种现象使模型的训练变得很复杂。所以在深度神经网络模型的训练中，通常需要仔细选取初始参数并采取较小的学习率，这不但导致模型训练的效率低下，而且使得饱和非线性模型的训练极为困难。我们把这种现象称为内部协变量转移(covariate shift)，并通过归一化(normalizing)每层的输入来解决这个问题。我们方法的强大之处在于把归一化的步骤作为模型训练架构的一部分来实现, 并且对每个训练小批量都执行归一化操作。批量归一化允许我们使用很高的学习率并且对初始化不太在意。它在一定情况下也可以起到正则化的作用，并减轻了对Dropout的需求。我们在最先进的图像分类模型中使用批量归一化法，在减少了14倍训练步骤的情况下实现了与原模型相同的精度，并以显著增量击败了原始模型。我们使用批量归一化的网络模型，增强了在ImageNet分类上发布的最佳结果:获得了4.9%前5验证误差（和4.8%测试误差），这超出了人类评估者的准确率。

* 文章下载:
 - PDF: Batch_Normalization/arx.pdf
 - WORD:Batch_Normalization/翻译稿WORD版.docx

