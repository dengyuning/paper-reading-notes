#### 阅读时间：2018年10月25日
#### 会议：http://cn.arxiv.org/pdf/1808.05759
#### 组织机构：微软和国防科大
#### 数据集：SQuAD 2.0

#### 论文简介:  
SQuAD2.0和SQuAD1.0最大的区别就在于，SQuAD2.0中有很多无法回答的问题。模型需要去判别数据集中哪些样本的问题是无法回答的。
> Previous works (Levy et al., 2017; Clark and Gardner, 2018) all apply a shared-normalization
operation between a “no-answer” score and answer span scores, so as to produce a probability that a question is unanswerable and output a candidate answer simultaneously.

本文的模型主要由两部分组成，一个是No-Answer Reader,负责从篇章中抽取正确答案（对answerable questions 和
unanswerable questions一视同仁）,另一个是Answer Verifier,对No-Answer Reader给出的答案进行评判。

* No-Answer Reader
模型结构暂不做详细介绍。主要有三个损失。
指针网络的输出和NA probability归一化得到的损失:
> Concretely, a shared softmax function can be applied to normalize both of no-answer score and span scores, yielding a joint no-answer objective defined as:
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/MRC/2018-10/Read_and_Verify_loss1.png?raw=true)

Independent Span Loss(独立的指针网络的损失):
> Therefore, besides answerable questions, we also include unanswerable cases as positive examples, and consider the plausible answer as gold answer.
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/MRC/2018-10/Read_and_Verify_loss2.png?raw=true)

Independent No-Answer Loss(独立的NA损失)
> Despite a multihead pointer network being used to prevent the confliction problem, no-answer detection can still be weakened since the no-answer score z is normalized with span scores. Therefore, we consider exclusively encouraging the prediction on no-answer detection.
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/MRC/2018-10/Read_and_Verify_loss3.png?raw=true)

* Answer Verifier
论文中设计了三种模型。这三种模型的输入都是[S;Q;$;A]。
第一种是Sequential Architecture，用到了Transformer的框架；
第二种是Interactive Architecture，计算了篇章和问句之间的一个注意力机制，最后用一个固定长度的向量来表示篇章;
第三种是Hybrid Architecture，将上述两个模型得到的篇章表示串接起来。

5. 模型框架：
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/MRC/2018-10/Read_and_Verify.png?raw=true)

6. 个人想法
重点在损失设计上。

7. 相关
