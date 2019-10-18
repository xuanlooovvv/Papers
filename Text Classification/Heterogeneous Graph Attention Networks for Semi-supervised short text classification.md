# Paper

- **Title**: Heterogeneous Graph Attention Networks for Semi-supervised Short Text Classification
- **Year**: 2019

# Summary

- What
  - 应用 GCN 的短文本分类任务
  - 针对短文本语义稀疏性、引入topics/entities外部信息，构造异构图（heterogeneous information network, HIN）
  - 普通GCN无法适用于异构图，提出异构图卷积(HGAT)
  - 引入dual-level attention mechanism
- How
  - 构造 异构图
    - Topics: 采用 LDA ，选取top P topics 与 short text 连接
    - Entities: 采用实体链接工具TAGME, 将实体与short text 连接，同时对于相似度高的实体也建立连接关系
      1. 已知上文出现的词汇，求下文出现某个词汇的概率
      2. 
  - 提出 异构图卷积
    - node初始化
      1. Document: TF-IDF vector
      2. Topic: 基于词表的概率分布
      3. Entity: 基于Wikipedia corpus的word2vec embedding 与 TF-IDF vector concat
    - 异构图卷积
      - 由于不同类型节点表示在不同特征空间，普通GCN无法应用， 提出heterogeneous graph convolution
      - 针对不同类型和不同节点，提出dual-level attention