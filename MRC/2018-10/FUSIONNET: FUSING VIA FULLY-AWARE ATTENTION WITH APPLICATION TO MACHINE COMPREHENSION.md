0. 阅读时间: 早  
1. 会议: ICLR2018  
2. 组织机构:  微软，国立台湾大学
3. 数据集:  SQuAD,SQuAD AddSent, SQuAD AddOneSent  
4. 论文简介:    
> Taking image recognition as an example, information in various levels of representations can 
capture different aspects of details in an image: pixel, stroke and shape. We argue that this hypothesis also holds 
in language understanding and MRC.  

> History-of-word can capture different levels of contextual information to fully understand the text.

每个词的HoW(history of word)是这个词的所有表示的串接在一起构成的向量。用历史词算出来的注意力机制，被称作
是 Fully-Aware Attention.

5. 模型框架:  
* 模型
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/FusionNet_model.png?raw=true)

* 跟以往attention的对比图
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/FusionNet_table1.png?raw=true)
(1) Word-level Fusion  
(2) High-level Fusion  
(2\`) High-level Fusion(Alternative)   
(3) Self-boosted fusion  
(3\`) Self-boosted fusion(Alternative)    

6. 个人想法:  
本文创新点在于信息交互层的设计。分析了以往注意力机制都是在哪一层展开的。然后引入History-of-word的概念，
考虑到不同语义空间上的信息(from low-level to high-level)。

7. 其他  
[代码](https://github.com/momohuang/FusionNet-NLI)
