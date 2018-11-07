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

* Document Reader:  

#### 个人想法:
工业上可采用的pipeline。

#### 其他:
