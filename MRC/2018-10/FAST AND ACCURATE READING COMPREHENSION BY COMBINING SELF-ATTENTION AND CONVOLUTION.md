0. 阅读时间: 早  
1. 会议: ICLR2018   
2. 组织机构: Google Brain, CMU  
3. 数据集: SQuAD

4. 论文简介:   
模型创新+数据增强(data augmentation)方法。  
* Embedding Encoder Layer:
> The encoder layer is a stack of the following basic building block: [convolution-layer x # + self-attention-layer + feed-forward-layer].
* Context-Query Attention Layer && Model Encoder Layer:
结合了DCN的注意力机制和BiDAF的注意力机制。

数据增强用的是back translation。即用机器翻译模型，把一句英文翻译成对应的K句法文，然后再把法文翻译成英文，这样
就得到了K^2句英文。只翻译(d,q,a)三元组中的d(文档)。

5. 模型框架:  
![image](https://github.com/dengyuning/paper-reading-notes/blob/master/paper_pictures/cnn_transformer.png?raw=true)

> In this paper, aiming to make the machine comprehension fast, we propose to remove the recurrent
nature of these models. We instead exclusively use convolutions and self-attentions as the building
blocks of encoders that separately encodes the query and context. Then we learn the interactions
between context and question by standard attentions (Xiong et al., 2016; Seo et al., 2016; Bahdanau
et al., 2015). The resulting representation is encoded again with our recurrency-free encoder before
finally decoding to the probability of each position being the start or end of the answer span.

6. 个人想法:
CNN对篇章建模，比RNN快。
transformer:没有用RNN，并行计算注意力机制，快。
在上下文表征层做的改动。

7. 其他
