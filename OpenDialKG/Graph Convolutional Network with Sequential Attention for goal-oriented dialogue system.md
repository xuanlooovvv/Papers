# Paper

- **Title**: Graph Convolutional Network with Sequential Attention for Goal-Oriented Dialogue Systems
- **Year**: 2019， Transactions of the Association for Computational Linguistics

# Summary

- What

  - 应用 GCN /结合KB 的对话系统

  - 将句子（通过依存分析树） 和 KB 用 GCN 表示

  - use a sequential attention mechanism

    

- How

  - GCN

    - rGCN引入过多参数

    - 这里只考虑三种不同类型的relation：

      u to v / v to u / u = v

  - Model

    - encoder

      1. Query Encoder: RNN-GCN
      2. Dialogue History Encoder: RNN-GCN
      3. KB Encoder: GCN

    - decoder 

      - Sequential Attention

        

        