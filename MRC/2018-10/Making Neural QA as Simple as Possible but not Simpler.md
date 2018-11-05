0. 阅读时间: 早  
1. 会议: CoNLL2017  
2. 组织机构: Language Technology Lab, DFKI  
3. 数据集: SQuAD, NewsQA and MsMARCO  
4. 论文简介:  
问题一: 有没有必要构建复杂模型？
> Increasingly complex systems have been conceived without comparison to a simpler
neural baseline system that would justify their complexity. 
> We further demonstrate, that an extended version (FastQAExt) achieves
state-of-the-art results on recent benchmark datasets, namely SQuAD, NewsQA
and MsMARCO, outperforming most existing models. However, we show that
increasing the complexity of FastQA to FastQAExt does not yield any systematic improvements.
> Although a variety of extractive QA systems have been proposed, there is no competitive neural
baseline. Most systems were built in what we call a top-down process that proposes a complex
architecture first and validates design decisions by an ablation study. Most ablation studies, however, remove only a single part of an overall complex architecture and therefore lack comparison to a reasonable neural baseline. This gap raises the question whether the complexity of current systems is justified solely by their empirical results.

5. 模型框架:   
Fig1 fastQA  
![image]()

Fig2  
![image]()


6. 个人想法:  
论文在探讨如何设计一个最简单的QA模型，从无到有，从最基本的模型开始入手搭建。

7. 其他   
【摘抄】   
> Each of those describe several innovations for the different layers of the architecture with a
special focus on developing powerful interaction layers.
