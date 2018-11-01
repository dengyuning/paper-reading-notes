0. 阅读时间：2018年3月2  
1. 会议：ICLR2018  
2. 组织机构：Salesforce Research  
3. 论文简介：  
We make two significant changes to the DCN by introducing a deep residual
coattention encoder and a mixed training objective that combines cross entropy loss from maximum
likelihood estimation and reinforcement learning rewards from self-critical policy learning.

4. 模型结构:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/DCN+_model1.png?raw=true)

![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/DCN+_loss.png?raw=true)

5. 个人想法:  
修改了信息交互层和答案层的损失函数。
> 信息交互层的工作，把DCN的计算过程堆叠了两次。把第一次注意力机制计算得到的特征、第二次注意力机制计算得到的特征，以及原有的篇章表示特征串接在一起，过一个双向LSTM，作为信息交互层最终的输出。
> 引入强化学习来提高F1值。

6. 其他:  
[DCN](https://github.com/dengyuning/paper-reading-notes/blob/master/MRC/2018-10/DYNAMIC%20COATTENTION%20NETWORKS%20FOR%20QUESTION%20ANSWERING.md)
