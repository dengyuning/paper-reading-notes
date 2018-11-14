#### 阅读时间: 早  
#### 会议: arXiv 2016  
#### 组织机构: IBM  
#### 数据集: SQuAD 1.0  
#### 论文简介:  
比较早的一篇论文。  

#### 模型框架:   
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/DCR_model.png?raw=true)

> DCR works in four steps. First, the encoder layer encodes passage and question separately, by using bidirectional recurrent
neural networks (RNN). Second, the attention layer calculates the relevance of each passage word to the question.
Third, the chunk representation layer dynamically extracts the candidate chunks from the given passage, and create
chunk representation that encodes the contextual information of each chunk. Fourth, the ranker layer scores the
relevance between the representations of a chunk and the given question, and ranks all candidate chunks using a softmax
layer.

特征表示层和信息交互层是常见的设计。
答案层，采用了

#### 个人想法:  
没有使用pointer layer来做。  

#### 其他
