0. 阅读时间: 2018年3月1日  
1. 会议: ICLR2017  
2. 组织机构: Salesforce Research  
3. 论文简介:   
论文的创新点在于*coattention encoder*和d*ynamic pointer decoder*.  

> We propose a coattention mechanism that attends to the question and document simultaneously,
similar to (Lu et al., 2016), and finally fuses both attention contexts.
> During each iteration, the decoder updates its state taking into account the coattention encoding corresponding to current estimates of the start and end positions, and produces, via a multilayer neural network, new estimates of the start and end positions.

4. 模型框架:
* 总体框架:
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/DCN_model.png?raw=true)

* 信息交互层:
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/DCN_attention.png?raw=true)

* 答案层:
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/DCN_decoder.png?raw=true)

5. 个人想法:   
信息交互层和答案层的创新。
* 信息交互层:
注意力机制这块的设计和attention over attention有一点相似的意味。

* 答案层:  
答案层用一个双向LSTM对篇章进行序列建模，每一个time step t，使用t-1时刻的hidden states 以及t-1时刻预测的开始和结束位置来作为信息，指导预测t时刻认为正确的开始和结束位置。
文中设计了一个Highway Maxout Network (HMN)来给篇章中每个词打分。

6. 其他:  
