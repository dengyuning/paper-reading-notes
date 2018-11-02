0. 阅读时间: 早  
1. 会议: arXiv  
2. 组织机构: Cornell University, Google   
3. 数据集: SQuAD,TriviaQA    
4. 论文简介:  
> In this work we propose, Gated Linear Dilated Residual Network (GLDR ), a different architecture
to avoid recurrent units in text precessing. More specifically, we use a combination of residual
networks (He et al., 2016), dilated convolutions (Yu & Koltun, 2016) and gated linear units (Dauphin
et al., 2017).

提出一个文本序列预处理的模块Conv。将BiDAF和Drqa模型中的RNN序列建模部分，替换成Conv。加速模型训练。

5. 模型框架:
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/convNets.png?raw=true)

6. 个人想法:  
文档表示方面的工作。通用模块设计。

7. 其他
