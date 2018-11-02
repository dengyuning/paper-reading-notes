0. 阅读时间：早  
1. 会议: ACL2017  
2. 机构: 北大，微软  
3. 论文简介:  
信息交互层有两个概念，一个是Gated Attention-based Recurrent Networks，一个是Self-Matching Attention。
* Gated Attention-based Recurrent Networks:  
用一个LSTM对篇章进行建模，每个time step的输入，是篇章串接上篇章对问句的注意力机制c_t。c_t的计算，考虑到LSTM上一个时刻的hidden states输出v_P_t-1，当前time step对应的token表示u_P_t，以及问句的表示u_Q。除此之外，设计了一个门，来动态地控制篇章当前时刻的输入u_P_t和c_t流入LSTM当前cell的一个信息量。

* Self-Matching Attention:  
用跟Gated Attention-based Recurrent Networks同样的方式，实现了一个自注意力机制。每个时刻，考虑到当前time step对 应的token表示v_P_t对整个篇章v_P的一个self attention。

4. 模型框架；
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/Gated_Self_Matching.png?raw=true)

5. 个人想法:
在信息交互层首次引入self attention的模型。

6. 相关:  
R-net模型图  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/R-net.png?raw=true)
