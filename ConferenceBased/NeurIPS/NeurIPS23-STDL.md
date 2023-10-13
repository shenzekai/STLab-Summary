# NeurIPS 2023 时空数据相关论文总结

**NeurIPS 2023将于2023年11月28日到12月9日在美国路易斯安那州新奥尔良举行。**

**根据官方公布的邮件显示，今年共有12343篇投稿，接受率为26.1%，官网显示一共有3564篇论文。**

**本文总结了NeurIPS 23时空数据的相关论文，由于目前官网只能看到标题和摘要，可能总结的不够全面，有部分论文挂在了arXiv上，就多补充了一些信息。欢迎大家补充，共同学习**。

### 1. Sparse Graph Learning from Spatiotemporal Time Series

**作者：**Andrea Cini, Daniele Zambon, Cesare Alippi

**链接：**https://neurips.cc/virtual/2023/poster/73924  **JMLR 2023**有篇相同的作者相同标题的文章：https://www.jmlr.org/papers/volume24/22-1154/22-1154.pdf

**关键词：**稀疏图、时空图预测

### 2. Equivariant Spatio-Temporal Attentive Graph Networks to Simulate Physical Dynamics

**作者：**Liming Wu, Zhichao Hou, Jirui Yuan, Yu Rong, Wenbing Huang

**链接：**https://neurips.cc/virtual/2023/poster/72921

**关键词：**AI4Science、时空图神经网络

**论文概述：**本文介绍了一种名为ESTAG的模型，用于表示和模拟物理系统的动力学。传统的基于图神经网络的方法在处理物理系统动力学时忽视了非马尔科夫性质，即忽视了系统与未观测到的对象之间的相互作用。为了解决这个问题，本文提出利用历史轨迹来反映潜在和未观察到的动力学，并将动力学模拟重新定义为时空预测任务。为了实现这一目标，本文设计了ESTAG模型，其中包括使用EDFT模块提取周期性特征，以及ESM和ETM模块用于处理空间和时间信息传递。最后再借助等变池化的操作将历史帧的信息进行融合作为模型的输出。实验证明，与传统的时空图神经网络和等变图神经网络相比，ESTAG在三个真实数据集上（分子级别、蛋白质级别、宏观运动级别）表现出更好的效果。

综上所述，本文提出的ESTAG模型充分考虑了物理系统的对称性和非马尔科夫性质，通过利用历史轨迹进行时空预测，为物理动力学建模提供了一种有效的方法。

来源人大高瓴公众号：https://mp.weixin.qq.com/s/gd_queWyVUk5jHKhXsbVlQ

### 3. Generative Pre-Training of Spatio-Temporal Graph Neural Networks

**作者：**Zhonghang Li, Lianghao Xia, Yong Xu, Chao Huang

**链接：**https://neurips.cc/virtual/2023/poster/70508

**关键词：**预训练、时空预测

### 4. Integration-free Training for Spatio-temporal Multimodal Covariate Deep Kernel Point Processes

**作者：**YIXUAN ZHANG, Quyu Kong, Feng Zhou

**链接：**https://neurips.cc/virtual/2023/poster/71268

**关键词：**多模态、点过程

### 5. What if We Enrich day-ahead Solar Irradiance Time Series Forecasting with Spatio-Temporal Context?

**作者：**Oussama Boussif, Ghait Boukachab, Dan Assouline, Stefano Massaroli, Tianle Yuan, Loubna Benabbou, **Yoshua Bengio**

**链接：**https://neurips.cc/virtual/2023/poster/70031  arXiv：[What if We Enrich day-ahead Solar Irradiance Time Series Forecasting with Spatio-Temporal Context?](https://arxiv.org/abs/2306.01112)

**代码：**https://github.com/gitbooo/CrossViVit

**关键词：**时空预测

### 6. Taming Local Effects in Graph-based Spatiotemporal Forecasting

**作者：**Andrea Cini, Ivan Marisca, Daniele Zambon, Cesare Alippi

**链接：**https://neurips.cc/virtual/2023/poster/70034  arXiv：[Taming Local Effects in Graph-based Spatiotemporal Forecasting](https://arxiv.org/abs/2302.04071)

**关键词：**时空图预测

### 7. DiffTraj: Generating GPS Trajectory with Diffusion Probabilistic Model

**作者：**Yuanshao Zhu, Yongchao Ye, Shiyao Zhang, Xiangyu Zhao, James Yu

**链接：**https://neurips.cc/virtual/2023/poster/69935  arXiv：https://arxiv.org/abs/2304.11582

**关键词：**扩散模型、轨迹生成

### 8. DYffusion: A Dynamics-informed Diffusion Model for Spatiotemporal Forecasting

**作者：**Salva Rühling Cachay, Bo Zhao, Hailey James, Rose Yu

**链接：**https://neurips.cc/virtual/2023/poster/71410 arXiv：https://arxiv.org/abs/2306.01984

**关键词：**扩散模型、时空预测

### 9. Automatic Integration for Spatiotemporal Neural Point Processes

**作者：**Zihao Zhou, Rose Yu

**链接：**https://neurips.cc/virtual/2023/poster/72359

**关键词：**时空点过程

### 10. Equivariant Neural Simulators for Stochastic Spatiotemporal Dynamics

**作者：**Koen Minartz, Yoeri Poels, Simon Koop, Vlado Menkovski

**链接：**https://neurips.cc/virtual/2023/poster/72442  arXiv：https://arxiv.org/abs/2305.14286

**关键词：**随机模拟、时空动态性

### 11. Deciphering Spatio-Temporal Graph Forecasting: A Causal Lens and Treatment

**作者：**Yutong Xia, Yuxuan Liang, Haomin Wen, Xu Liu, Kun Wang, Zhengyang Zhou, Roger Zimmermann

**链接：**https://neurips.cc/virtual/2023/poster/73036  arXiv：https://arxiv.org/abs/2309.13378

**关键词：**时空预测、因果推断

### Dataset and Benchmark

### 12. Fine-Grained Spatio-Temporal Particulate Matter Dataset From Delhi For ML based Modeling

**作者：**Sachin Chauhan, Zeel Bharatkumar Patel, Sayan Ranu, Rijurekha Sen, Nipun Batra

**链接：**https://neurips.cc/virtual/2023/poster/73476

**关键词：**空气质量数据集

### 13. UUKG: Unified Urban Knowledge Graph Dataset for Urban Spatiotemporal Prediction

**作者：**Yansong Ning, Hao Liu, Hao Wang, Zhenyu Zeng, Hui Xiong

**关键词：**知识图谱、时空预测

**链接：**https://neurips.cc/virtual/2023/poster/73440  arXiv：[UUKG: Unified Urban Knowledge Graph Dataset for Urban Spatiotemporal Prediction](https://arxiv.org/abs/2306.11443)

**代码：**https://github.com/usail-hkust/UUKG

### 14. OpenSTL: A Comprehensive Benchmark of Spatio-Temporal Predictive Learning

**作者：**Cheng Tan, Siyuan Li, Zhangyang Gao, Wenfei Guan, Zedong Wang, Zicheng Liu, Lirong Wu, Stan Z. Li

**链接：**https://neurips.cc/virtual/2023/poster/73674  arXiv：[OpenSTL: A Comprehensive Benchmark of Spatio-Temporal Predictive Learning](https://arxiv.org/abs/2306.11249)

**关键词：**时空预测、benchmark

**代码：**https://github.com/chengtan9907/OpenSTL

### 15. LargeST: A Benchmark Dataset for Large-Scale Traffic Forecasting

**作者：**Xu Liu, Yutong Xia, Yuxuan Liang, Junfeng Hu, Yiwei Wang, LEI BAI, Chao Huang, Zhenguang Liu, Bryan Hooi, Roger Zimmermann

**链接：**https://neurips.cc/virtual/2023/poster/73480 arXiv：https://arxiv.org/abs/2306.08259

**代码：**https://github.com/liuxu77/LargeST

**关键词：**大规模、交通预测

### 16. Creating High-Fidelity Synthetic GPS Trajectory Dataset for Urban Mobility Analysis

**作者：**Yuanshao Zhu, Yongchao Ye, Ying Wu, Xiangyu Zhao, James Yu

**链接：**https://neurips.cc/virtual/2023/poster/73469

**关键词：**GPS轨迹数据集

### **相关链接：**

**NeurIPS 2023全部论文列表：**https://neurips.cc/virtual/2023/papers.html

[NeurIPS 2023 时间序列论文汇总](https://zhuanlan.zhihu.com/p/659088918)

[KDD 2023 时空数据论文](https://zhuanlan.zhihu.com/p/650189765)

[ICDE 2023 时空数据论文](https://zhuanlan.zhihu.com/p/656129320)

[WWW 2023 时空数据论文](https://zhuanlan.zhihu.com/p/657027003)

[ECML PKDD 2023 时空数据论文](https://zhuanlan.zhihu.com/p/658052428)

[CIKM 2023 时空数据论文总结](https://zhuanlan.zhihu.com/p/655169678)

[AAAI 2023时空数据学习相关论文汇总](https://mp.weixin.qq.com/s/pAiYMnekcDc_pcI7YFSqYg)

[KDD 2022时空数据挖掘领域论文汇总](https://mp.weixin.qq.com/s/9mvHsUCvhMwphaLGmILzYw)



