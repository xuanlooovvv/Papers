# Paper

* **Title**: XLNet: Generalized Autoregressive Pretraining for Language Understanding
* **Year**: 2019

# Summary

* What
  * 对于BERT的改进
  * 基于Auto Regressive语言模型，而非BERT的Auto Encoder
  * 提出了Permutation LM(排列语言模型)

* How
  * Method
    * Auto Regressive LM:
      1. 已知上文出现的词汇，求下文出现某个词汇的概率
      2. 
  * Permutation LM(排列语言模型)
    * 排列
      * 长度为T的序列x，有T!种排列方式
      * 对于不同的排列方式，参数是共享的
    * 采样
      * 由于计算复杂度的限制，实际训练时对每个输入序列只采用一个采样的排列方式
  * Transfomer-XL
    * 截断长文本
