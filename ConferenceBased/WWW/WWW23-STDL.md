# WWW 2023 时空数据论文汇总

WWW 23于2023年4月30日-5月4日在美国德克萨斯州奥斯汀举行。此次会议共收到1900篇投稿，录用率约为19.2%。

本文汇总了WWW 23有关时空数据论文的论文，找来找去就4篇纯时空的论文（不包含时序），感觉较少。如有疏漏，欢迎大家补充（提issue）。

## Automated Spatio-Temporal Graph Contrastive Learning

**作者：**Qianru Zhang, Chao Huang, Lianghao Xia, Zheng Wang, Zhonghang Li, Siuming Yiu

**论文链接：**

arXiv：https://arxiv.org/abs/2305.03920

ACM：https://arxiv.org/pdf/2305.03920.pdf

**代码：**https://github.com/HKUDS/AutoST

**一作在paperweekly的解读：**[WWW 2023 | 预训练时空模型新范式](https://mp.weixin.qq.com/s/VaU3w_Ln7aUQYqnkg1NmAg)

**关键词：**对比学习，时空预测

**论文简介：**在各种区域嵌入方法中，基于图的区域关系学习模型因其强大的结构表示能力而脱颖而出，可以使用图神经网络编码空间相关性。 尽管它们很有效，但现有方法还没有很好地解决几个关键挑战：i）由于多种因素，数据噪声和缺失在许多时空场景中普遍存在。 ii）输入时空数据（例如，移动轨迹）通常表现出跨空间和时间的分布异质性。 在这种情况下，当前的方法容易受到生成的区域图的质量的影响，这可能会导致性能不佳。 在本文中，通过在多视图数据源生成的异构区域图上探索自动时空图对比学习范式（AutoST）来解决上述挑战。 AutoST 框架建立在异构图神经架构之上，用于捕获 POI 语义、移动流模式和地理位置方面的多视图区域依赖性。 为了提高 GNN 编码器针对数据噪声和分布问题的鲁棒性，还设计了一种带有参数化对比视图生成器的自动时空增强方案。 AutoST可以适应时空异构图，并且多视图语义得到很好的保留。 在几个真实数据集上对三个下游时空挖掘任务进行的广泛实验表明， AutoST 在各种基线上取得了显着的性能提升。 

![AutoST](https://gitee.com/bestZKS/note-pic/raw/master/img/20230918211648.png)

## INCREASE: Inductive Graph Representation Learning for Spatio-Temporal Kriging

**作者：** Chuanpan Zheng, Xiaoliang Fan, Cheng Wang, Jianzhong Qi, Chaochao Chen and Longbiao Chen

**论文链接：**

arXiv：https://arxiv.org/abs/2302.02738

ACM：https://dl.acm.org/doi/abs/10.1145/3543507.3583525

**代码：**https://github.com/zhengchuanpan/INCREASE

**关键词：**克里金（kriging）方法，交通预测,表示学习

**公众号解读：**[WWW'23 | 归纳式图表示学习的时空克里金插值方法INCREASE](https://mp.weixin.qq.com/s/30xPLN2N9l_gw5l1OH6ADA)

**论文简介：**时空克里金法是网络和社交应用中的一个重要问题，例如网络或物联网，其中连接到网络的事物（例如传感器）通常具有空间和时间属性。 它的目的是使用给定感兴趣时间段内观察到的位置（的事物）的数据来推断未观察到的位置（的事物）的知识。 这个问题本质上需要归纳学习。 经过训练后，模型应该能够对不同位置（包括新给定的位置）执行克里金法，而无需重新训练。 然而，由于异构的空间关系和不同的时间模式，执行准确的克里金法结果具有挑战性。 在本文中，提出了一种新颖的时空克里金归纳图表示学习模型。 首先通过空间邻近性、功能相似性和转移概率对未观察到的位置和观察到的位置之间的异构空间关系进行编码。 基于每个关系，准确地聚合最相关的观察位置的信息，通过联合建模它们的相似性和差异，为未观察到的位置产生归纳表示。 然后，设计关系感知门控循环单元（GRU）网络来自适应捕获每个关系生成的序列表示中的时间相关性。 最后，提出了一种多关系注意机制，可以动态融合多个关系中不同时间步长的复杂时空信息，以计算克里金输出。 三个现实世界数据集的实验结果表明，提出的模型始终优于最先进的方法，并且当观察到的位置较少时，优势更加显著。 

![INCREASE](https://gitee.com/bestZKS/note-pic/raw/master/img/20230918212552.png)

## Learning to Simulate Daily Activities via Modeling Dynamic Human Needs

**作者：**Yuan Yuan, Huandong Wang, Jingtao Ding, Depeng Jin and Yong Li

**论文链接：**

ACM：https://dl.acm.org/doi/abs/10.1145/3543507.3583276

arXiv：https://arxiv.org/abs/2302.10897

**代码：**https://github.com/tsinghua-fib-lab/Activity-Simulation-SAND

**关键词：**人类活动仿真

**论文简介：**记录个人日常生活中各类活动的日常活动数据被广泛应用于活动调度、活动推荐、政策制定等众多应用中。 尽管其价值很高，但由于收集成本高和潜在的隐私问题，其可访问性受到限制。 因此，模拟人类活动产生海量高质量数据对于实际应用具有重要意义。 然而，现有的解决方案，包括简化人类行为假设的基于规则的方法和直接拟合现实世界数据的数据驱动方法，都无法完全符合现实。 在本文中，受经典心理学理论——描述人类动机的马斯洛需求理论的启发，本文提出了一种基于生成对抗性模仿学习的知识驱动模拟框架。 为了增强生成的活动数据的保真度和实用性，核心思想是将人类需求的演变建模为模拟模型中驱动活动生成的基本机制。 具体来说，这是通过分解不同需求级别的分层模型结构以及成功捕获需求动态的分段连续特征的神经随机微分方程的使用来实现的。 大量的实验表明，该框架在数据保真度和实用性方面优于最先进的基线。 此外，还提出了需求建模的富有洞察力的可解释性。 

![SAND](https://gitee.com/bestZKS/note-pic/raw/master/img/20230918215123.png)

## Learning Social Meta-knowledge for Nowcasting Human Mobility in Disaster

**作者**：Renhe Jiang, Zhaonan Wang, Yudong Tao, Chuang Yang, Xuan Song, Ryosuke Shibasaki, Shu-Ching Chen and Mei-Ling Shyu

**论文链接：**

ACM：https://dl.acm.org/doi/abs/10.1145/3543507.3583991

researchgate：https://www.researchgate.net/profile/Chuang-Yang-3/publication/370413276_Learning_Social_Meta-knowledge_for_Nowcasting_Human_Mobility_in_Disaster/links/64527c334af78873525714e7/Learning-Social-Meta-knowledge-for-Nowcasting-Human-Mobility-in-Disaster.pdf

**代码：**https://github.com/deepkashiwa20/MemeSTN

**关键词：**人类移动性，时空预测

**论文简介：**人员流动临近预报是智能交通规划、灾害应对和管理等方面的基础研究问题。特别是飓风、流行病等重大灾害下的人员流动在很大程度上偏离了日常生活，这使得该任务更具挑战性。 现有的工作主要集中在正常情况下的交通或人群流量预测。 为了解决这个问题，在本研究中，与灾难相关的 Twitter 数据被纳入作为协变量，以了解公众对灾难事件的认识和关注，从而了解其对人员流动的影响。 因此，提出了一种元知识可记忆时空网络（MemeSTN），它利用记忆网络和元学习来融合社交媒体和人类移动数据。 对日本 2019 年台风季节、日本 2020 年 COVID-19 大流行和美国 2019 年飓风季节等三种现实灾难进行了广泛的实验，以说明提出的解决方案的有效性。 与最先进的时空深度模型和多元时间序列深度模型相比，模型可以在国家级和州级灾难情况下的临近预报人员流动性方面取得优异的性能。

![MeMeSTN](https://gitee.com/bestZKS/note-pic/raw/master/img/20230918214349.png)

相关链接：

WWW 2023 全部接收论文:[WWW 2023 Accepted Paper](https://archives.iw3c2.org/www2023/program/accepted-papers/)

[KDD 2023 时空数据相关论文](https://zhuanlan.zhihu.com/p/650189765)

[如何看待 ICDE2023的审稿结果和录取情况?](https://www.zhihu.com/question/549012748/answer/3210102049)

[CIKM 2023 时空数据论文总结](https://zhuanlan.zhihu.com/p/655169678)

[AAAI 2023时空数据学习相关论文汇总](https://mp.weixin.qq.com/s/pAiYMnekcDc_pcI7YFSqYg)

[KDD 2022时空数据挖掘领域论文汇总](https://mp.weixin.qq.com/s/9mvHsUCvhMwphaLGmILzYw)