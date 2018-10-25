### 阅读时间：2018年10月25日
### 会议：ICLR2017
### 组织机构：CMU
### 数据集：CBT, Who Did What

### 论文简介:
* WORD-CHARACTER FINE-GRAINED GATING（特征表示层的工作）：
利用Token的其他信息，构造了一个门，来动态地进行词向量和字向量的特征组合。
Token的其他信息包括：
> named entity tags, part-of-speech tags, binned document frequency vectors, and the word-level representations.

论文中对此的解释是：
> Though Miyamoto & Cho (2016) also use a gate to choose between word-level and character-level
representations, our method is different in two ways. First, we use a more fine-grained gating mechanism, i.e., vector gates rather than scalar gates. Second, we condition the gate on features that better reflect the properties of the token. For example, for noun phrases and entities, we would expect the gate to bias towards character-level representations because noun phrases and entities are usually less common and display richer morphological structure. Experiments show that these changes are key to the performance improvements for reading comprehension tasks.

* DOCUMENT-QUERY FINE-GRAINED GATING（信息交互层的工作）:
1. Attention over attention 中的注意力机制:   
dot product 计算相似度; 篇章中每个词和问句中每个词都进行计算，属于pair-wise.
2. The Gated Attention Reader 中的注意力机制:  
element-wise product;给篇章中的每个词的表示一个权重，代表这个词的重要性.
3. 本文的注意力机制(详见模型框架图2):   
both pair-wise and element-wise.

### 模型框架：  

![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/words_or_chars_gate1.png?raw=true)

![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/words_or_chars_gate2.png?raw=true)

### 个人想法: 
在【特征表示层】和【信息交互层】做的改动。性能提升不明显。

### 相关  
[论文代码](https://github.com/kimiyoung/fg-gating)
