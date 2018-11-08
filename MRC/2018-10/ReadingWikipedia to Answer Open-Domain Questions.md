#### 阅读时间: 早
#### 会议: ACL2017
#### 组织机构: 斯坦福和Facebook AI
#### 数据集: SQuAD, CuratedTREC, WebQuestions, WikiMovies
#### 论文简介: 
* 创新点:
> This paper proposes to tackle opendomain question answering using Wikipedia as the unique knowledge
source: the answer to any factoid question is a text span in a Wikipedia article.
> Our approach combines a search component based on bigram hashing and TF-IDF matching with a multi-layer recurrent neural network model trained to detect answers in Wikipedia paragraphs.

可应用于开放域问答的通用模型框架，由Document Retriever和Document Reader构成。  
给定一个问题，由Document Retriever检索回相关文档或篇章，再由Document Reader在篇章中抽取正确答案。  

#### 模型框架:
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/Drqa_model.png?raw=true)

* Document Retriever:   
没有写的特别详细，有提到用TF-IDF来线性加权词向量特征，局部的词序和n-gram特征也有用到。

* Document Reader:    
1. 特征表示层: 词向量，exact match, pos特征, ner特征, tf词频特征, 篇章中的每个词都学到了问句的一个聚合表示, 串接到原本的特征表示向量后面.   
2. 上下文表示层:问句做一个self attention,得到一个固定长度的问句表示q.    
3. 答案层:问句表示q做了线性变化后，和篇章中的每个词的表示进行点乘。  

 
#### 个人想法:  
工业上可采用的pipeline。  

#### 其他:
1. [WikiExtractor script]: (https://github.com/attardi/wikiextractor).
2. [CuratedTREC]: (https://github.com/brmson/dataset-factoid-curated).
3. [YodaQA]: (https://github.com/brmson/yodaqa/wiki/Benchmarks)


#### 其他:
