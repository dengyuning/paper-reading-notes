#### 阅读时间: 早  
#### 会议:  SemEval-2018
#### 组织机构:  Yuanfudao Research
#### 数据集: SemEval-2018   
#### 论文简介:   
SemEval-2018评测上获胜团队的论文。模型创新+融合外部知识。
> The relation is determined by querying ConceptNet whether there is an edge between Pi and any
word in question Q or answer A . If there exist multiple different relations, just randomly choose one.

#### 模型框架:  
![image](https://github.com/intfloat/commonsense-rc/blob/master/image/TriAN.jpg)

1. 特征表示层:   
Glove词向量,POS特征向量,NER特征向量,关系向量,logarithmic term frequency feature and co-occurrence feature
(篇章中这个词是否在问句或答案选项中出现过)   
2. 信息交互层: word-level attention    
计算了Question-aware passage representation,passage-aware answer representation和question-aware answer representa
tion三种注意力。之后用双向LSTM进行聚合。  
3. 答案层:  
用self-attention对问句和答案的表示进行聚合，最终答案决策的时候考虑到问句、答案和篇章三者的信息。


#### 个人想法:    
引入的外部知识比较新颖独特。   
答案、篇章、问句的注意力机制只考虑了单向。  
term frequency是用英文维基百科计算的。  

#### 其他:  
[SemEval榜单](https://competitions.codalab.org/competitions/17184#results)
[代码](https://github.com/intfloat/commonsense-rc)
【资源】:ConceptNet, WebChild,DeScript
【相关论文】:
[Reasoning with heterogeneous knowledge for commonsense machine comprehension](http://aclweb.org/anthology/D17-1216)
[Leveraging Knowledge Bases in LSTMs for Improving Machine Reading](http://aclweb.org/anthology/P17-1132)
