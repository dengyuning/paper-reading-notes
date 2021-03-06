0. 阅读时间：2018年10月17日
1. 数据集：RACE
2. 组织机构：新加坡国立大学 IBM
3. 会议：ACL2018
4. 模型：
* 特征表示层：词向量
* 上下文建模层：双向LSTM对篇章、问句、答案候选项分别进行建模，得到篇章表示H\^P、问题表示H\^Q和答案表示H\^A。
* 信息交互层（模型的创新点）: 
> 1. 计算篇章和问句的注意力G\^Q，得到H^Q' = H^Q * G\^Q
> 2. 计算篇章和答案的注意力G\^A，得到H^A' = H^A * G\^A
> 3. 拿H^Q'和H^A'分别和篇章原有表示H^P进行交互（点积、相减构成两个特征，然后进行非线性变换），最后得到的特征串接起来，作为篇章的新表示C。
> 4. 具体对篇章进行序列建模过程中，对每个句子分别进行1、2、3上述操作，然后将每个句子的C_i表示过一个最大池化。将句子表示集合串接到一起后，过完双向LSTM然后最大池化，得到篇章的最后表示h_t。
* 答案选择层:
h_t是篇章、问句和某个答案候选项的匹配表示。最后将所有答案候选项和篇章的匹配表示计算出来，求出概率最大值。

5. 性能：
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/MRC/2018-10/2018_10_1.png?raw=true)

6. 个人想法：
有点点新奇的地方是把整个篇章分句子处理。
分别考虑到了篇章对问句的注意力、篇章对答案的注意力。计算对象有两个，但是计算过程是单向的。即没有考虑问句对篇章的注意力，也没有考虑答案对篇章的注意力。
没有问句和答案之间的一个交互。
注意力计算挺简单的，不复杂，不过有时候简单或许更好。

7. 相关：
* [论文链接](http://aclweb.org/anthology/P18-2118)
* [论文代码](https://github.com/shuohangwang/comatch)

@InProceedings{P18-2118,
  author = 	"Wang, Shuohang
		and Yu, Mo
		and Jiang, Jing
		and Chang, Shiyu",
  title = 	"A Co-Matching Model for Multi-choice Reading Comprehension",
  booktitle = 	"Proceedings of the 56th Annual Meeting of the Association for Computational Linguistics (Volume 2: Short Papers)",
  year = 	"2018",
  publisher = 	"Association for Computational Linguistics",
  pages = 	"746--751",
  location = 	"Melbourne, Australia",
  url = 	"http://aclweb.org/anthology/P18-2118"
}

