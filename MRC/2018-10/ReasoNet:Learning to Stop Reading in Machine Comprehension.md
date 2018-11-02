0. 阅读时间:  早

1. 会议:  ACM

2. 组织机构:  微软

3. 数据集: CNN/Daily Mail, SQuAD, Graph Reachability

4. 论文简介:  
>  Our proposed approach explores the idea of using both attentionsum to aggregate candidate 
attention scores and multiple turns to attain a better reasoning capability.  

模型由五部分组成:Memory,Attention,Internal State,Termination Gate和Answer。

* Memory&Attention:
CNN/Daily Mail: (Mdoc,Mques) 问句和篇章过完双向LSTM之后的hiddenstates。Memory和当前time step的状态s_t计算。
SQuAD: 篇章过完信息交互层之后的表示（利用Coattention机制融合了问句信息）
Graph Reachability: 篇章过完双向LSTM之后的特征

* Internal State:  
用篇章过完双向LSTM得到的每个time step的hidden states作为状态值s_t.

* Termination Gate:  
利用每个time step的状态值s_t来过一个逻辑回归，进行二分类，判断要不要停下来。

5. 模型框架:    
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/ReasoNet_model.png?raw=true)

6. 个人想法:     
最优化算法用到了强化学习。引入了memory机制。

7. 相关:  
【摘抄】
> Meanwhile, the analysis in [3] also illustrates the huge variations in the difficulty level with 
respect to questions in the CNN/Daily Mail datasets [7].
