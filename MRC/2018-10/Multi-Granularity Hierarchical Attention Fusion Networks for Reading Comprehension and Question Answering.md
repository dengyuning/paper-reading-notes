#### 阅读时间: 2018年11月14日  
#### 会议: ACL2018  
#### 组织机构: 阿里  
#### 数据集: SQuAD 2.0,TriviaQA, AddSent, AddOne-Sent  
#### 论文简介:
论文发表时在SQuAD2.0榜单上排名第一。  
> It consists of several parts: a basic co-attention layer with shallow semantic fusion, a self-attention layer with deep semantic fusion and a memorywise bilinear alignment function.
> The proposed network has two distinctive characteristics: (i) A fine-grained fusion approach to blend attention vectors for a better understanding of the relationship between question and passage; (ii) A multi-granularity attention mechanism applied at the word and sentence-level, enabling it to properly attend to the most important content when constructing the question and passage representation.


特征表示层设计了残差连接，把token的char embedding串接到双向LSTM得到的特征embedding后。
主要工作在于信息交互层。首先计算co-attention，利用篇章对问句的注意力来aggregate问句的信息，利用问句对篇章的注意力来aggregate篇章的信息。计算了串接、差值(difference)和点乘(element-wise product)三种特征，用Fuse操作来
挖掘新特征。在此基础上，设计了一个gate来自动选择是用原本的特征表示，还是注意力计算之后得到的新表示。


#### 模型框架:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/HAFN_model.png?raw=true)

#### 个人想法:   
co-attention这个思想，导师和我都有想到过。  

#### 其他:  
