0. 阅读时间: 早  
1. 会议: AAAI2018  
2. 组织机构: National University of Singapore  
3. 论文简介:
论文模型有两处亮点。
> We propose a multi-factor attentive encoding approach based on tensor transformation to 
synthesize meaningful evidence across multiple sentences.

本质上相当于多个语义空间的self-attention机制。用W矩阵计算了m个角度的相似度，求出最大值作为最后的相似度矩阵F~。用矩阵F~  和篇章原本的表示V相乘，得到新的篇章表示M~。在此基础上，设计了一个门，来动态控制M~的信息流。

> To subsume fine-grained answer type information, we propose a max-attentional question 
aggregation mechanism which learns to identify the meaningful portions of a question.  

设计了两个问题的特征。  
对于篇章和问句的相似度矩阵A(T行U列)，首先按列求最大值，然后过一个softmax层，得到K。用K聚合问句表示得到q_ma,视作The maxattentional question representation。  
把问句中wh类型词和紧接着wh词的那个词的表示作为q_f，视作问题类型表示。

4. 模型框架:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/Question_focused.png?raw=true)

5. 个人想法:   
工作主要集中在信息交互层。多角度进行注意力机制的计算。

6. 相关:  
[代码](https://github.com/nusnlp/amanda)
