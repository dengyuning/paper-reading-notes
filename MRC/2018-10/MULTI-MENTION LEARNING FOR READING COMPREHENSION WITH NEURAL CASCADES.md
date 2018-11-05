#### 阅读时间:  早
#### 会议:  ICLR2018
#### 组织机构: CMU,google research
#### 数据集:  TriviaQA   
#### 论文简介:  
1. a non-recurrent architecture enabling processing of longer evidence texts consisting of simple
submodels.
2. the aggregation of evidence from multiple mentions of answer candidates at the representation level.
3. the use of a multi-loss objective.

#### 模型框架:   
![image]()

* LEVEL 1: AVERAGED BAGS OF EMBEDDINGS:
0. span embeddings:
词向量加权平均串接上二元特征0-1表示当前span包含问题中的Token与否,得到span表示R
1. QUESTION + SPAN (M1):   
首先利用self-attention机制计算得到question表示Q,R和S串接过一层仿射变换，再过一层线性变换计算得到span的得分s1。
2. SPAN + SHORT CONTEXT (M2):   
对span左右的上下文词向量平均，得到span所在上下文的表示。串接上span表示，计算得到span的得分s2。

* LEVEL 2: ATTENDING TO THE CONTEXT (M3)
* LEVEL 3: AGGREGATING MULTIPLE MENTIONS (M4)

6. 个人想法:   
特别简单的模型。模型由很多子模型构成，每个子模型只包含全连接神经网络以及注意力机制。子模型可以并行。

7. 相关:
