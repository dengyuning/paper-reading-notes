#### 阅读时间: 早
#### 会议: IJCAI 2018
#### 组织机构: 复旦，微软
#### 数据集:  SQuAD1.0, AddSent, AddOneSent
#### 论文简介:  
信息交互层的创新+强化学习优化F1值  

* 现在的注意力机制存在的问题:
> However, in these approaches, the current attention is unaware of which parts of the context
and question have been focused in earlier attentions, which results in two distinct but related issues, where
multiple attentions 1) focuses on same texts, leading to attention redundancy and 2) fail to focus on some salient
parts of the input, causing attention deficiency.
* 现在的强化学习策略存在的问题:
> Specifically, an estimated baseline is utilized to normalize the reward and reduce variances. However, the convergence
can be suppressed when the baseline is better than the reward. This is harmful if the inferior reward
is partially overlapped with the ground truth, as the normalized objective will discourage the prediction
of ground truth positions. We refer to this case as the convergence suppression problem.

#### 模型框架:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/Reinforced_Mnemonic_Reader_model.png?raw=true)
多轮的注意力机制  
拿之前的注意力机制来修改当前的注意力机制    

#### 个人想法:  
对注意力机制理解的比较好  
#### 其他:  
