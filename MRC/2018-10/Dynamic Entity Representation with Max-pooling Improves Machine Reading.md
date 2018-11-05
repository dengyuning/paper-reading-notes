0. 阅读时间:早
1. 会议:  NAACL2016
2. 组织机构: Tohoku University, Japan  
3. 数据集:  CNN/Daily Mail
4. 论文简介: 
> In this paper, we hypothesize that a reader without world knowledge can only understand a named en
tity by dynamically constructing its meaning from the contexts.
本文给出现在篇章中的每一个实体学习到一个向量表示。
假设实体e在文章上下文c1、c2和c3处都出现过(c1、c2、c3都是句子)。将c1过一个双向LSTM，得到句子表示后再过一个非线性层(tanh),
记做ce1。同理得到ce2和ce3。将这三个表示用学到的权重系数W（和问句表示计算注意力机制得到）进行线性加权，得到最终实体e的表示。

5. 模型框架:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/dynamic_entity_repre.png?raw=true)

6. 个人想法:  
ICLR2018有一篇类似论文

7. 其他:  
[代码](https://github.com/soskek/der-network)
