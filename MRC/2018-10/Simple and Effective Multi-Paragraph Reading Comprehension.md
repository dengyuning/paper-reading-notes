0. 阅读时间: 早
1. 会议:  ACL2018
2. 组织机构: Allen Institute
3. 论文简介:  
在经典模型Bidaf的基础上引入了self attention机制。设计了四种处理训练篇章的方式。
增加了NAloss来判断一个篇章有没有可能包含答案。   
* Shared-Normalization    
每个段落单独作为一个篇章进行训练，最后预测答案时，在M个段落上进行归一化。跟把M个段落串接在一起，作为一个统一的篇章
来处理有点像。但是这样处理的时候，段落之间没有信息交互的过程。  

* Merge  
各个段落用分割符串接到一起。  
> Our motive is to test whether simply exposing the model to more text will teach the model to be more
adept at ignoring irrelevant text.

* No-Answer Option  
计算每个篇章包含答案的可能性。

* Sigmoid
对每个词，计算它作为开始或结束位置的一个概率值，然后对每个词计算一个交叉熵损失。
> The intuition is that, since the scores are being evaluated independently of one another, they will be 
comparable between different paragraphs.

4. 模型框架:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/bidaf_self_att.png?raw=true)

5. 个人想法:  
基于对任务认识的数据预处理，信息交互层的改进和答案层损失的设计。

6. 相关:  
[代码](https://github.com/allenai/document-qa)
