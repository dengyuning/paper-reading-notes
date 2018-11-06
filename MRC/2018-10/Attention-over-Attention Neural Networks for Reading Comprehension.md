#### 阅读时间: 早  
#### 会议: ACL2016  
#### 组织机构: 哈工大和科大讯飞  
#### 数据集: CNN和Daily Mail  
#### 论文简介:   
1. To our knowledge, this is the first time that the mechanism of nesting another attention
over the existing attentions is proposed, i.e. attention-over-attention mechanism.  
2. Unlike the previous works on introducing complex architectures or many non-trainable
hyper-parameters to the model, our model is much more simple but outperforms various 
state-of-the-art systems by a large margin.  
3. We also propose an N-best re-ranking strategy to re-score the candidates in various aspects
and further improve the performance.

#### 模型框架:
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/Attention_over_attention.png?raw=true)  

#### 个人想法:  
完形填空式的阅读理解任务。基于注意力机制的注意力。利用注意力机制来给篇章中每个词计算它作为答案的得分。

#### 相关  
