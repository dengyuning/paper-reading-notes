### 阅读时间：2018年10月27日    

### 会议: [arixiv](https://arxiv.org/pdf/1810.06683v1.pdf)    

### 组织机构: California Institute of Technology,Allen Institute for Artificial Intelligence,University of Washington    

### 数据集: CoQA,QuAC    

### 论文简介:  

* 研究背景：  
论文中谈到了基于单轮数据集开发的MRC模型的基本框架，继而延伸到现有的multi-turn任务上的模型为了适应现有的single-turn数据集的通用框架，把之前的question/answer pairs的信息融合到当前的question和document的表示中。针对现有multi-turn模型存在的问题，作者提出了自己的新方法：

  > Initially the word embeddings (e.g., Pennington et al., 2014; Peters et al., 2018) of
question tokensQand context tokens C are taken as input and fed into contextual integration layers,
such as LSTMs (Hochreiter & Schmidhuber, 1997) or self attentions (Yu et al., 2018), to encode the
question and context. Multiple integration layers provide contextualized representations of context,
and are often inter-weaved with attention, which inject question information. The context integration
layers thus produce a series of query-aware hidden vectors for each word in the context. Together,
the context integration layers can be viewed as conducting implicit reasoning to find the answer candidates. The final output is fed into the answer prediction layer to select the answer.


### 模型框架:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/FlowQA_model.png?raw=true)    

0. Integration Flow Layer:(这块没太看懂)
对于每个问句来说，有一个篇章的表示D_i。i代表的是当前对话的轮数。

1. QUESTION/CONTEXT ENCODING

2.

### 个人想法:  
> 以后读论文，看到一个新的数据集，可以先自己思考一下这个数据集是用来解决什么问题的，应用场景是什么，最大的难点在哪。可以先自己构思下模型的设计，再对比其和论文中模型的优缺点。

### 相关：
