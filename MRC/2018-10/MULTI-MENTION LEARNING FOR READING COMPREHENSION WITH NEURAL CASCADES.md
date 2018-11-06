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
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/multi_mention_model.png?raw=true)

![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/multi_mention_complexity.png?raw=true)

* LEVEL 1: AVERAGED BAGS OF EMBEDDINGS:
0. span embeddings:
词向量加权平均串接上二元特征0-1表示当前span包含问题中的Token与否,得到span表示R
1. QUESTION + SPAN (M1):   
首先利用self-attention机制计算得到question表示Q,R和S串接过一层仿射变换，再过一层线性变换计算得到span的得分s1。
2. SPAN + SHORT CONTEXT (M2):   
对span左右的上下文词向量平均，得到span所在上下文的表示。串接上span表示，计算得到span的得分s2。

* LEVEL 2: ATTENDING TO THE CONTEXT (M3)  
用包含span s的句子，和问句进行注意力计算。把M1和M2得到的表示和attention之后得到的句子表示、问句表示进行串接，得到M3表示，然后计算span的得分s3。 

* LEVEL 3: AGGREGATING MULTIPLE MENTIONS (M4)
把多处包含span s的表示进行聚合，进行打分，得到span的最终得分s4。

#### 个人想法:   
特别简单的模型。模型由很多子模型构成，每个子模型只包含全连接神经网络、非线性变换以及注意力机制。子模型可以并行。

#### 相关:
