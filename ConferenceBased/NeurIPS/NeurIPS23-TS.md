# NeurIPS 2023 时间序列相关论文总结

【就蹭一下NeurIPS刚放榜的热度吧，再总结一篇NeurIPS有关时间序列的文章】

祝大家中秋国庆双节快乐！

**NeurIPS 2023将于11月28日到12月9日在美国路易斯安那州新奥尔良举行。**

**根据官方公布的邮件显示，今年共有12343篇投稿，接受率为26.1%，官网显示一共有3564篇论文。**

**本文总结了NeurIPS 23 时间序列（不含时空数据，已经另外总结）的相关论文，由于目前官网只能看到标题和摘要，可能总结的不够全面，有部分论文挂在了arXiv上，就多补充了一些信息。欢迎大家补充，共同学习。**

### 1. WITRAN: Water-wave Information Transmission and Recurrent Acceleration Network for Long-range Time Series Forecasting （Spotlight）

**作者：**Yuxin Jia, Youfang Lin, Xinyan Hao, Yan Lin, Shengnan Guo, Huaiyu Wan

**链接**：https://neurips.cc/virtual/2023/poster/69972

**关键词：**长时预测

**代码：**https://github.com/Water2sea/WITRAN

**论文简介：**捕获语义信息对于长程时间序列的准确预测至关重要，其中包括两大方面：（1）建模全局和局部相关性，（2）挖掘长期和短期的重复模式。以往的研究工作能够一定程度上捕获这些方面中的一部分，但无法完成它们的同时捕获。此外，以往研究工作的时间和空间复杂性仍然很高。

基于此，我们提出了一种新颖的水波信息传递（Water-wave Information Transmission，简称WIT）框架，能够通过双粒度的信息传递捕捉短期和长期的重复模式。在WIT框架中，我们设计了一种新型水平垂直门控选择单元（Horizontal Vertical Gated Selective Unit，简称HVGSU），通过循环地融合和选择信息，来建模全局和局部相关性。此外，在提高计算效率方面，我们提出了一种通用的循环加速网络（Recurrent Acceleration Network，简称RAN），能够在保证空间复杂度为O(L)的同时，将时间复杂度降低到为O(√L)。

综上，我们将提出的方法命名为：水波信息传递和循环加速网络（Water-wave Information Transmission and Recurrent Acceleration Network，简称WITRAN）。通过在能源、交通、天气等领域的四个大型公开数据集上的实验证明，相对于现有方法，WITRAN在长程和超长程时间序列预测任务上成为了最佳方法（SOTA）。

Spotlight信息来源北京交通大学网络科学与智能系统研究所公众号：[喜报 | 我所两篇论文被机器学习领域顶会NeurIPS 2023接收](https://mp.weixin.qq.com/s/kkNEpZOAn9MFUGg5P9ZfXQ)

### 2. Sparse Deep Learning for Time Series Data: Theory and Applications

**作者：**Mingxuan Zhang, Yan Sun, Faming Liang

**链接：**https://neurips.cc/virtual/2023/poster/72629 

**关键词：**稀疏学习、感觉像是综述

### 3. Causal Discovery from Subsampled Time Series with Proxy Variables

**作者：**Mingzhou Liu, Xinwei Sun, Lingjing Hu, Yizhou Wang

**链接：**https://neurips.cc/virtual/2023/poster/70936     arXiv：[Causal Discovery from Subsampled Time Series with Proxy Variables](https://arxiv.org/abs/2305.05276)

**关键词**：因果发现  

### 4. Causal Discovery in Semi-Stationary Time Series

**作者：**Shanyun Gao, Raghavendra Addanki, Tong Yu, Ryan Rossi, Murat Kocaoglu

**链接：**https://neurips.cc/virtual/2023/poster/71016

**关键词：**因果发现、半平稳时间序列

### 5. Frequency-domain MLPs are More Effective Learners in Time Series Forecasting

**作者：**Kun Yi, Qi Zhang, Wei Fan, Hui He, Pengyang Wang, Shoujin Wang, Ning An, Defu Lian, Longbing Cao, Zhendong Niu

**链接：**https://neurips.cc/virtual/2023/poster/70726

**关键词：**频域、MLP(疑似又是化繁为简的工作，类似DLinear)

### 6. FourierGNN: Rethinking Multivariate Time Series Forecasting from a Pure Graph Perspective

**作者：**Kun Yi, Qi Zhang, Wei Fan, Hui He, Liang Hu, Pengyang Wang, Ning An, Longbing Cao, Zhendong Niu

**链接：**https://neurips.cc/virtual/2023/poster/71159

**关键词：**图神经网络、多元时间序列预测

### 7. CrossGNN: Confronting Noisy Multivariate Time Series Via Cross Interaction Refinement

**作者：**qihe huang, Lei Shen, Ruixin Zhang, Shouhong Ding, Binwu Wang, Zhengyang Zhou, Yang Wang

**链接：**https://neurips.cc/virtual/2023/poster/70010

**关键词：**图神经网络、多元时间序列预测

### 8. Scale-teaching: Robust Multi-scale Training for Time Series Classification with Noisy Labels

**作者：**Zhen Liu, ma peitian, Dongliang Chen, Wenbin Pei, Qianli Ma

**链接：**https://neurips.cc/virtual/2023/poster/72608

**关键词：**时间序列分类、鲁棒性

### 9. Time Series as Images: Vision Transformer for Irregularly Sampled Time Series

**作者：**Zekun Li, Shiyang Li, Xifeng Yan

**链接：**https://neurips.cc/virtual/2023/poster/71219 arXiv：https://arxiv.org/abs/2303.12799 （看格式是ICML改投的）

**代码：**https://github.com/Leezekun/ViTST

**关键词：**VIT

### 10. Adaptive Normalization for Non-stationary Time Series Forecasting: A Temporal Slice Perspective

**作者：**Zhiding Liu, Mingyue Cheng, Zhi Li, Zhenya Huang, Qi Liu, Yanhu Xie, Enhong Chen

**链接：**https://neurips.cc/virtual/2023/poster/72816

**关键词**：非平稳时间序列预测

### 11. Koopa: Learning Non-stationary Time Series Dynamics with Koopman Predictors

**作者：**Yong Liu, Chenyu Li, Jianmin Wang, Mingsheng Long

**链接：**https://neurips.cc/virtual/2023/poster/72562      arXiv：https://arxiv.org/abs/2305.18803

**关键词：**非平稳时间序列预测

### 12.  SimMTM: A Simple Pre-Training Framework for Masked Time-Series Modeling（Spotlight）

**作者：**Jiaxiang Dong, Haixu Wu, Haoran Zhang, Li Zhang, Jianmin Wang, **Mingsheng Long**

**链接：** [SimMTM: A Simple Pre-Training Framework for Masked Time-Series Modeling](https://neurips.cc/virtual/2023/poster/70829) arXiv：https://arxiv.org/abs/2302.00861

**关键词：**预训练、统一框架建模

### 13. WildfireSpreadTS: A dataset of multi-modal time series for wildfire spread prediction

**作者：**Sebastian Gerard, Yu Zhao, Josephine Sullivan

**链接：**https://neurips.cc/virtual/2023/poster/73593

**关键词：**多模态时间序列、数据集

### 14. Drift doesn't Matter: Dynamic Decomposition with Diffusion Reconstruction for Unstable Multivariate Time Series Anomaly Detection

**作者：**Chengsen Wang, Qi Qi, Jingyu Wang, Haifeng Sun, Xingyu Wang, Zirui Zhuang, Jianxin Liao

**链接：**https://neurips.cc/virtual/2023/poster/71195

**关键词：**多元时间序列异常检测

### 15. Nominality Score Conditioned Time Series Anomaly Detection by Point/Sequential Reconstruction

**作者：**Chih-Yu Lai, Fan-Keng Sun, Zhengqi Gao, Jeffrey H Lang, Duane Boning

**链接：**https://neurips.cc/virtual/2023/poster/70582

**关键词：**时间序列异常检测

### 16. MEMTO: Memory-guided Transformer for Multivariate Time Series Anomaly Detection

**作者：**Junho Song, Keonwoo Kim, Jeonglyul Oh, Sungzoon Cho

**链接：**https://neurips.cc/virtual/2023/poster/71519

**关键词：**时间序列异常检测

### 17. Conformal Prediction for Time Series with Modern Hopfield Networks

**作者：**Andreas Auer, Martin Gauch, Daniel Klotz, **Sepp Hochreiter**（LSTM一作）

**链接：** https://neurips.cc/virtual/2023/poster/72007  arXiv：https://arxiv.org/abs/2303.12783

**关键词：**共性预测、霍普菲尔德网络

### 18. Conformal Scorecasting: Anticipatory Uncertainty Quantification for Distribution Shift in Time Series

**作者：**Anastasios Angelopoulos, Ryan Tibshirani, **Emmanuel Candes**

**链接：**https://neurips.cc/virtual/2023/poster/69896

**关键词：**共性预测、不确定性量化

### 19. Finding Order in Chaos: A Novel Data Augmentation Method for Time Series in Contrastive Learning

**作者：**Berken Utku Demirel, Christian Holz

**链接：**https://neurips.cc/virtual/2023/poster/71014  arXiv：https://arxiv.org/abs/2309.13439

**关键词：**对比学习、数据增强

### 20. ContiFormer: Continuous-Time Transformer for Irregular Time Series Modeling

**作者：**Yuqi Chen, Kan Ren, Yansen Wang, Yuchen Fang, Weiwei Sun, Dongsheng Li

**链接：**https://neurips.cc/virtual/2023/poster/71304

**关键词：**（喜闻乐见的）Former改动、不规则时间序列

### 21. BasisFormer: Attention-based Time Series Forecasting with Learnable and Interpretable Basis

**链接：**https://neurips.cc/virtual/2023/poster/69976

**关键词：**（喜闻乐见的）Former改动、时间序列预测

### 22. Time Series Kernels based on Nonlinear Vector AutoRegressive Delay Embeddings

**作者：**Giovanni De Felice, John Goulermas, Vladimir Gusev

**链接：**https://neurips.cc/virtual/2023/poster/71521

**关键词：**核方法

### 23. Predict, Refine, Synthesize: Self-Guiding Diffusion Models for Probabilistic Time Series Forecasting

**作者：**Marcel Kollovieh, Abdul Fatir Ansari, Michael Bohlke-Schneider, Jasper Zschiegner, Hao Wang, Yuyang (Bernie) Wang

**链接：**https://neurips.cc/virtual/2023/poster/70377  arXiv：https://arxiv.org/abs/2307.11494

**关键词：**扩散模型、时间序列预测

### 24. OneNet: Enhancing Time Series Forecasting Models under Concept Drift by Online Ensembling

**作者：**yifan zhang, Qingsong Wen, xue wang, Weiqi Chen, Liang Sun, Zhang Zhang, Liang Wang, **Rong Jin, Tieniu Tan**

**链接：**https://neurips.cc/virtual/2023/poster/71725   arXiv：[OneNet: Enhancing Time Series Forecasting Models under Concept Drift by Online Ensembling](https://arxiv.org/abs/2309.12659)

**代码：**https://github.com/yfzhang114/OneNet

**关键词**：时间序列预测、概念漂移

### 25. One Fits All: Power General Time Series Analysis by Pretrained LM

这篇热度之前应该就很高，在各大平台应该都有针对的解读

**作者：**Tian Zhou（FEDFormer（ICML 22） FilM(NeurIPS 22)一作）, Peisong Niu, xue wang, **Liang Sun**, **Rong Jin**

**链接：**https://neurips.cc/virtual/2023/poster/70856    [Researchgate](https://www.researchgate.net/profile/Tian-Zhou-18/publication/368753168_One_Fits_AllPower_General_Time_Series_Analysis_by_Pretrained_LM/links/647d80e3b3dfd73b77662460/One-Fits-AllPower-General-Time-Series-Analysis-by-Pretrained-LM.pdf)

**关键词：**大模型、时间序列统一任务

### 26. Large Language Models Are Zero Shot Time Series Forecasters

**作者：**Marc Finzi, Nate Gruver, Shikai Qiu, Andrew Wilson

**链接：**https://neurips.cc/virtual/2023/poster/70543

**关键词：**大模型、零样本、时间预测

### 27. Contrast Everything: Multi-Granularity Representation Learning for Medical Time-Series

**作者：**Yihe Wang, Yu Han, Haishuai Wang, Xiang Zhang

**链接：**https://neurips.cc/virtual/2023/poster/70272

**关键词：**对比学习、医疗时间序列

### 28. FOCAL: Contrastive Learning for Multimodal Time-Series Sensing Signals in Factorized Orthogonal Latent Space

**作者：**Shengzhong Liu, Tomoyoshi Kimura, Dongxin Liu, Ruijie Wang, Jinyang Li, Suhas Diggavi, Mani Srivastava, Tarek Abdelzaher

**链接：**https://neurips.cc/virtual/2023/poster/70617

**关键词：**对比学习、多模态时间序列

### 29. BioMassters: A Benchmark Dataset for Forest Biomass Estimation using Multi-modal Satellite Time-series

**作者：**Andrea Nascetti, Ritu Yadav, Kirill Brodt, Qixun Qu, Hongwei Fan, Yuri Shendryk, Isha Shah, Christine Chung

**链接：**https://neurips.cc/virtual/2023/poster/73499

**关键词：**数据集、多模态

### 30. Encoding Time-Series Explanations through Self-Supervised Model Behavior Consistency

**作者：**Owen Queen, Thomas Hartvigsen, Teddy Koker, Huan He, Theodoros Tsiligkaridis, Marinka Zitnik

**链接：**https://neurips.cc/virtual/2023/poster/69958  arXiv：[Encoding Time-Series Explanations through Self-Supervised Model Behavior Consistency](https://arxiv.org/abs/2306.02109)

**关键词：**可解释性、自监督

### 31. On the Constrained Time-Series Generation Problem

**作者：**Andrea Coletta, Sriram Gopalakrishnan, Daniel Borrajo, Svitlana Vyetrenko

**链接：**[On the Constrained Time-Series Generation Problem](https://neurips.cc/virtual/2023/poster/72006)  arXiv：[On the Constrained Time-Series Generation Problem](https://arxiv.org/abs/2307.01717)

**关键词：**时间序列生成、扩散模型

### **相关链接：**

**NeurIPS 2023全部论文列表：**https://neurips.cc/virtual/2023/papers.html