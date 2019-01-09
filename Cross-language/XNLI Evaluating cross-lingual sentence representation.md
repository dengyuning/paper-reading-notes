### XNLI:Evaluating Cross-lingual Sentence Representation  
### 阅读时间: 2019年1月  
### 机构: Facebook AI, NYU  
### 数据集: XNLI  
### 论文创新点:  
提出了一个新的跨语言任务：跨语言文本蕴含。

> XNLI consists of 7500 human-annotated development and test examples in NLI three-way classification format in English, French, Spanish,
German, Greek, Bulgarian, Russian, Turkish, Arabic, Vietnamese, Thai, Chinese, Hindi, Swahili and Urdu, making a total of 112,500 annotated pairs.

### 模型:  
1. Translate Train(Strong Baseline) 
2. Translate Test(Strong Baseline)
3. pretrained universal multilingual sentence embeddings based on the average of word embeddings (X-CBOW)
4. bidirectional-LSTM sentence encoders trained on the MultiNLI training data (X-BILSTM) 

### 相关工作:  
* Multilingual Word Embeddings  
 
* Sentence Representation Learning  
 
* Multilingual Sentence Representations  
 
*  Cross-lingual Evaluation Benchmarks  
  
### 相关:  
跨语言情感分类 cross-lingual document classification  
  
  
