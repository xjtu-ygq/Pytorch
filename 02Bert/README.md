# bert

* 预训练
* 微调

## 如何使用bert

主要介绍第一次如何使用bert，这里借助分类任务（其他task类似），你只需要关注主要步骤：

* step1 导包
* step2 读取并处理数据
* step3 获取bert预训练模型（来自官网https://huggingface.co）
* step4 数据加载
* step5 模型定义
* step6 损失函数和优化器
* step7 训练、验证、测试

可以看到，与主流框架几乎一致，只多出了**获取bert预训练模型**

* 预训练是指，大数据集上已经训练好的数据（比如分词，每个词对应的id等）和模型
* 数据加载中用到了tokenizer，是借助预训练对数据进行分词（在以往自己处理数据时是需要自己处理token的，这里更加简便）
* 模型定义中，将bert的模型直接加进去，再根据自己的任务稍作处理即可

因此，如何使用bert，请牢记一下要点：

* 获取对应的预训练模型（step3）
* tokenizer使用预训练模型即可(step4)
* 将bert模型直接加入自己的模型(step5)

代码些许生涩，请根据上述三点**针对性阅读**即可，其他部分代码可以跳过

## 关于bert的tricks

* Last 4 Layers Concatenating
* 模型层间差分学习率
* ITPT

## 参考

* https://arxiv.org/abs/1905.05583
* https://www.bilibili.com/video/BV1v64y1x7dp