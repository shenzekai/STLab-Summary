**第39届IEEE数据工程国际会议（ICDE2023 ）于4月3日到7日在美国加利福尼亚州召开。本届ICDE共接收论文228篇，录用率在25%左右。本文总结了ICDE 2023上有关时空数据的工作。如有疏漏，欢迎大家补充。**

本文参考“时空数据学习”的推文做了进一步补充：

原文链接：https://mp.weixin.qq.com/s/MQ-T11QP39Qibn1nwTk57g

## Research track

### 1. Online Anomalous Subtrajectory Detection on Road Networks with Deep Reinforcement Learning

**作者：**Qianru Zhang (The University of Hong Kong)*; ZHENG WANG (Nanyang Technological University); Cheng Long (Nanyang Technological University); Chao Huang (University of Hong Kong); S.M. Yiu (The University of Hong Kong); Yiding Liu (Baidu Inc.); Gao Cong (Nanyang Technological Univesity); Jieming Shi (The Hong Kong Polytechnic University)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184886

**代码：**https://github.com/lizzyhku/OASD

**关键词：**异常检测、强化学习

**一句话概括：**本文提出了一种新的基于强化学习的异常轨迹检测的解决方案RL4OASD，以在线方式检测异常子轨迹，是一种依赖于无标签数据的数据驱动方法。

**论文简介：**在许多基于位置的应用中，检测异常轨迹已经成为一项重要任务。虽然针对这项任务提出了许多方法，但它们都存在各种问题，包括(1)无法检测异常子轨迹，这些异常子轨迹是轨迹数据中的细粒度异常，(2)非数据驱动，(3)需要足够的监督标签，这些标签的收集成本很高。在本文中，作者提出了一种新的基于强化学习的解决方案RL4OASD，它避免了现有方法的所有上述问题。RL4OASD包括两个网络，一个负责学习道路网络和轨迹的特征，另一个负责根据学习到的特征检测异常子轨迹，这两个网络可以在没有标记数据的情况下迭代训练。在两个真实数据集上进行了大量的实验，结果表明，本文的解决方案可以显著优于最先进的方法(提高20-30%)，并且可以高效地在线检测(处理每个新生成的数据点所需时间小于0.1ms)。

![图1 RL4OASD](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919142525.png)

### 2. When Spatio-Temporal Meet Wavelets: Disentangled Traffic Forecasting via Efficient Spectral Graph Attention Networks

**作者：**Yuchen Fang (Beijing University of Posts and Telecommunications)*; Yanjun Qin (Beijing University of Posts and Telecommunications); Haiyong Luo (Research Center for Ubiquitous Computing Systems, Institute of Computing Technology, Chinese Academy of Sciences); Fang Zhao (School of Software Engineering, Beijing University of Posts and Telecommunications); Bingbing Xu ( Institute of Computing Technology,University of Chinese Academy of Sciences); Liang Zeng (Tsinghua University); Chenxing Wang (Beijing University of Posts and Telecommunications)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184591

**代码：**https://github.com/LMissher/STWave

**关键词：**交通预测，DTW

**一句话概括：**提供了一种新颖的去纠缠融合框架STWave来缓解分布偏移问题，还将一种新颖的查询采样策略和基于图小波的图位置编码融入到完整的图注意力网络中，从而高效且有效地建模动态空间相关性。

**论文简介：**交通预测对公共安全和资源优化至关重要，但由于交通数据的时间变化和动态空间相关性，交通预测非常具有挑战性。为捕获这些复杂的依赖关系，人们应用了时空网络，例如具有图卷积网络的循环神经网络、具有时间卷积网络的图卷积网络以及具有全图注意力网络的时间注意力网络。然而，之前的时空网络基于端到端的训练，因此无法处理非平稳交通时间序列中的分布偏移。另外，现有网络中仍缺乏高效且有效的空间相关性建模算法。

本文的目标不是提出另一种端到端模型，而是提供一种新颖的去纠缠融合框架STWave来缓解分布偏移问题。该框架首先将复杂的交通数据解耦为稳定趋势和波动事件，然后通过双通道时空网络分别对趋势和事件进行建模。最后，通过趋势和事件的融合来预测合理的未来流量。此外，作者将一种新颖的查询采样策略和基于图小波的图位置编码融入到完整的图注意力网络中，从而高效且有效地建模动态空间相关性。在6个交通数据集上的广泛实验表明了本文提出的方法的优越性，即以较低的计算成本获得较高的预测精度。

![图2 STWave](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919191820.png)

### 3. BERT-Trip: Effective and Scalable Trip Representation using Attentive Contrast Learning

**作者：**Ai-Te Kuo (Auburn University)*; Haiquan Chen (California State University, Sacramento); Wei-Shinn Ku (Auburn University)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184553

**代码：**https://github.com/KuoAite/BERT-Trip

**关键词：**POI推荐，对比学习

**一句话概括：**提出了一个自监督对比学习框架BERT-Trip来学习有效且可扩展的行程表示，以支持时间敏感和用户个性化的行程推荐。

**论文简介：**在过去的十年中，行程推荐引起了相当大的关注。在行程推荐中，针对给定查询推荐一系列兴趣点( POI )，其中包括出发点和目的地。近年来，注意力机制的出现以及许多融入注意力的模型在各个领域都取得了巨大的成功。行程推荐问题表现出类似的特征，可以从注意力机制中潜在获益。然而，将注意力机制应用于行程推荐并非易事。本文有动力回答以下两个研究问题：（1）如何在没有标签的情况下有效地学习行程表征？与大多数自然语言处理任务不同，行程推荐没有可用的真实标签。（2）如何在无手工制作负样本的情况下有效学习行程表征？在本文中，作者将行程表示学习转化为自然语言处理( NLP )任务，提出了一个自监督对比学习框架BERT-Trip来学习有效且可扩展的行程表示，以支持时间敏感和用户个性化的行程推荐。BERT-Trip基于孪生网络构建，使用BERT作为主干编码器，以最大化行程增强之间的相似性。作者利用掩码策略在孪生网络中生成行程的增强视图(正样本对)，并在孪生网络的一侧使用停止梯度来消除使用任何负样本对或动量编码器的需要。在现实世界数据集上的大量实验表明，BERT-Trip在所有有效性指标上始终优于最先进的方法。与最先进的方法相比，BERT-Trip在Flickr和Weeplaces数据集上的F1分数分别提高了24%和40%。同时本文还提供了BERT-Trip可扩展至12800个POI的严格性能评估。

![图3 BERT-Trip](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921100344.png)

### 4. A Contextual Master-Slave Framework on Urban Region Graph for Urban Village Detection

**作者：**Congxi Xiao (University of Science and Technology of China); Jingbo Zhou (Baidu Inc.)*; Jizhou Huang (Baidu); Hengshu Zhu (Baidu); Tong Xu (University of Science and Technology of China); Dejing Dou (Baidu); Hui Xiong (The Hong Kong University of Science and Technology (Guangzhou))

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184898

**关键词：**城中村检测，POI

**一句话概括：**本文提出了一种上下文主从框架（CMSF），从城市整体区域图和不同区域的基础模型构建主从模型，从而提升城中村检测的能力。

**论文介绍：**城中村是指城市中落后于快速城市化的欠发达的非正式定居点。由于这些城中村存在高度的社会不平等和社会风险，城市管理者能发现所有城中村对于制定适当的改造政策至关重要。现有的检测城中村的方法是劳动密集型的，没有完全解决城中村检测中的独特挑战，例如标记城中村的稀缺性和不同地区的不同城市模式。为此，本文首先构建了一个城市区域图（URG），以分层结构的方式对城市区域进行建模。此后，本文设计了一种新颖的上下文主从框架来有效地从城市区域图中检测城中村。这种框架的核心思想是首先在城市区域图上预训练基础模型（主模型），然后从不同区域的基础模型自适应地导出特定模型（从模型）。该框架可以通过学习在城市地区城中村检测的通用性和特异性之间取得平衡。在三个城市上进行的广泛实验，证明了该框架的有效性。

![图4 CMSF](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921095222.png)

### 5. RNTrajRec: Road Network Enhanced Trajectory Recovery with Spatial-Temporal Transformer

**论文链接：** https://ieeexplore.ieee.org/abstract/document/10184766/

**代码：**https://github.com/chenyuqi990215/RNTrajRec

**作者：**Yuqi Chen (Fudan University); Hanyuan Zhang (Fudan University); Weiwei Sun (” Fudan University, China”)*; Baihua Zheng (Singapore Management University)

**关键词：**轨迹生成（恢复）

**一句话概括：**本文介绍了一种名为RNTrajRec的轨迹恢复方法，该方法考虑了道路网络的拓扑结构，通过增强GPS点的空间信息，实现了更高的准确性和空间一致性。

**论文简介：**GPS轨迹是许多基于轨迹应用的重要基础，如旅行时间估计、交通预测和轨迹相似性测量等。大多数应用需要大量高采样率的轨迹以实现良好性能。然而，由于节能考虑或其他约束，实际生活中收集的轨迹采样率较低。本文研究了轨迹恢复任务，用来提升轨迹的采样率。目前，大多数现有的轨迹恢复工作都遵循seq2seq架构，其中一个编码器用于编码轨迹，一个解码器用于恢复轨迹中的真实GPS点。然而，这些工作只使用网格信息或原始GPS点作为输入，忽略了道路网络的拓扑结构。因此，编码器模型无法捕捉轨迹GPS点周围的丰富空间信息，导致预测不够准确且空间一致性较低。在本文中，提出了一种基于道路网络增强的transformer框架用于轨迹恢复，即RNTrajRec。RNTrajRec首先使用图模型（GridGNN）学习每个道路段的嵌入特征。接下来，提出了一个空间-时间transformer模型，即GPSFormer，以学习轨迹的丰富空间和时间特征，并带有一个子图生成模块，以捕捉轨迹中每个GPS点的空间特征。最后，它将编码器模型的输出应用到一个多任务解码器模型，以恢复丢失的GPS点。在三个大规模实际轨迹数据集的大量实验证明了方法的有效性。

![图5 RNTrajRec](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921151421.png)

### 6. Self-supervised Trajectory Representation Learning with Temporal Regularities and Travel Semantics

**作者：** Jiawei Jiang (Beihang University)*; Dayan Pan (Beihang University); Houxing Ren (Beihang University); Xiaohan Jiang (Beihang University); Chao Li (Beihang University); Jingyuan Wang (Beihang University)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184736

**代码：**https://github.com/aptx1231/START

**“时空数据学习”公众号已有解读：**https://mp.weixin.qq.com/s/bU8e4LDSsZEjJ-PKrxqOtg

**关键词：**轨迹表示学习、自监督学习

**一句话概括：**文章提出了一种具有时间规则性和行程语义的自监督轨迹表示学习框架。

**论文简介：**轨迹表示学习（Trajectory Representation Learning, TRL）是时空数据分析和管理的强大工具。轨迹表示学习旨在将复杂的原始轨迹转换为低维表示向量，可应用于各种下游任务，如轨迹分类、聚类和相似度计算。现有工作通常将轨迹视为普通的序列数据，而蕴含在轨迹中的一些时空特征，如时间规律性和旅行语义，并未得到充分利用，为了充分挖掘出轨迹中的时间规律和旅行语义，本文提出了一个新的自监督轨迹表示学习框架START。其包括两个阶段，第一阶段是轨迹模式增强图注意力网络（TPE-GAT），将路网特征和旅行语义转换为路段的表示向量；第二阶段是时间感知轨迹编码器（TAT-Enc），将轨迹中路段的表示编码并融合轨迹的时间规律得到轨迹的表示。此外，还设计了两个自监督任务，即跨度屏蔽轨迹恢复和轨迹对比学习，以将轨迹的时空特征引入训练过程。两个真实数据集的三个下游任务的实验结果证明了START的优越性。

**一句话概括：**文章提出了一种具有时间规则性和行程语义的自监督轨迹表示学习框架。

**论文简介：**轨迹表示学习（Trajectory Representation Learning, TRL）是时空数据分析和管理的强大工具。轨迹表示学习旨在将复杂的原始轨迹转换为低维表示向量，可应用于各种下游任务，如轨迹分类、聚类和相似度计算。现有工作通常将轨迹视为普通的序列数据，而蕴含在轨迹中的一些时空特征，如时间规律性和旅行语义，并未得到充分利用，为了充分挖掘出轨迹中的时间规律和旅行语义，本文提出了一个新的自监督轨迹表示学习框架START。其包括两个阶段，第一阶段是轨迹模式增强图注意力网络（TPE-GAT），将路网特征和旅行语义转换为路段的表示向量；第二阶段是时间感知轨迹编码器（TAT-Enc），将轨迹中路段的表示编码并融合轨迹的时间规律得到轨迹的表示。此外，还设计了两个自监督任务，即跨度屏蔽轨迹恢复和轨迹对比学习，以将轨迹的时空特征引入训练过程。两个真实数据集的三个下游任务的实验结果证明了START的优越性。

![图6 START](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921150830.png)

### 7. Uncertainty Quantification for Traffic Forecasting: A Unified Approach.

**作者：**Weizhu Qian (Aalborg University)*; Dalin Zhang (Aalborg University); Yan Zhao (Aalborg University); Kai Zheng (University of Electronic Science and Technology of China); James Yu (Southern University of Science and Technology)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184566

**关键词：**不确定性量化，交通预测

**一句话概括：**提出一种对交通预测不确定性量化的统一方法DeepSTUQ，并提出一种新的模型校准机制提高了量化性能。无论是在点估计还是量化（区间估计）性能上均取得了最好的效果

**论文简介：**不确定性是时间序列预测任务中一个关键的考量因素。在这项研究中，着重于量化交通预测的不确定性。为了达到这个目标，提出了深度时空不确定性量化（DeepSTUQ）方法，它能够估计数据和模型两种不确定性。首先，利用一个时空模型来模拟交通数据中的复杂时空相关性。然后，建立了两个独立的最大化异构对数似然的子神经网络来估计数据不确定性。结合变分推理和深度集成的优势，分别通过整合MC-Dropout和自适应权重平均再训练方法来估计模型不确定性。最后，提出了一种基于温度系数（Temperature Scaling）的后处理校准方法，提高了模型估计不确定性的泛化能力。在四个公共数据集上进行了大量的实验，实验结果表明，该方法在点预测和点计算方面都优于最先进的方法。

![图7 DeepSTUQ](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919150539.png)

### 8. Extreme-Aware Local-Global Attention for Spatio-Temporal Urban Mobility Learning

**作者：**Huiqun Huang (University of Connecticut); Suining He (The University of Connecticut)*; Mahan Tabatabaie (University of Connecticut)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184645

**关键词：**天气预测，异常检测

**一句话概括：**天气、节假日等异常事件可以显著影响城市交通运动模式，本文提出了一种量化极端值的方法，并融入人口移动模式预测，提高了预测的准确性。

**论文简介：**精准的人口移动模式预测依赖于对异常事件的合理建模，因此，如何量化对异常事件和因素对人口出行模式的影响极为重要且有着挑战性。本文针对如何建模出行模式的局部性和全局性以及如何在预测任务中融入重尾分布的异常事件影响因素，提出了融合极端值的局部-全局注意力的出行量预测模型EALGAP，EALGAP模拟了不同区域的流动性和时间步长的时空全局和局部影响，用于不同城市区域的流动性预测。通过提取不同区域的移动系统的总体或规则的空间依赖性和时间模式来考虑全局影响。在四个不同的移动数据集（总共超过1300万次旅行）进行了广泛的实验研究，这些数据来自美国的两个异常自然或社会事件（如飓风事件、其他极端天气条件和联邦假日）。实验结果表明了EALGAP的准确性，有效性和感知极端的能力。

![图8 EALGAP](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921100950.png)

### 9. ROI-demand Traffic Prediction: A Pre-train, Query and Fine-tune Framework

**作者：**Yue Cui (The Hong Kong University of Science and Technology)*; Shuhao Li (Guangzhou University); Wenjin Deng (University of Electronic Science and Technology of China); Zhaokun Zhang (University of Electronic Science and Technology of China); Jing ZHAO (HKUST); Kai Zheng (University of Electronic Science and Technology of China); Xiaofang Zhou (The Hong Kong University of Science and Technology)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184520

**关键词：**交通预测，预训练、微调

**一句话概括：**提出了一种名为TQT的预训练、查询和微调框架，用于ROI-demand交通预测，通过定制输入数据和快速微调预训练模型，实现了有效和高效的交通预测。

**论文简介：**本文主要解决了ROI-demand Trafﬁc Prediction (RTP)的问题。该问题是指在给定任何查询感兴趣区域（Region of Interest, ROI）的情况下，预测其未来的交通情况。为了解决这个问题，论文提出了一种名为TQT的预训练、查询和微调的框架。该框架首先根据ROI自定义输入数据，然后通过微调预训练的交通预测模型进行快速适应。论文在两个真实世界的交通数据集上对TQT进行了评估，包括流量和速度预测任务。广泛的实验结果表明了该方法的有效性和效率。

![图9 TQT](https://gitee.com/bestZKS/note-pic/raw/master/img/20230920102427.png)

### 10. Self-Supervised Spatial-Temporal Bottleneck Attentive Network for Efficient Long-term Traffic Forecasting

**作者：**Shengnan Guo (Beijing Jiaotong University)*; Youfang Lin (Beijing Jiaotong University); Letian Gong (Beijing Jiaotong University); Chenyu Wang (Beijing Jiaotong University); Zeyu Zhou (Beijing Jiaotong University); Zekai Shen (Beijing Jiaotong University); YiHeng Huang (Beijing Jiaotong University); Huaiyu Wan (Beijing Jiaotong University)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184658/

**代码：**https://github.com/guoshnBJTU/SSTBAN

**关键词：**自监督学习，长时（交通）预测

**一句话概括：**本文提出了一种自监督时空瓶颈注意力网络SSTBAN有效解决了长时交通预测问题。

**论文摘要：**在智能交通系统（ITS）中，长期交通预测的准确性对于辅助城市管理者和交通参与者做出明智决策具有重要意义。然而，现有的时空预测模型在应用于长期交通预测时，其精度会显著下降，主要原因在于这些模型难以有效地捕捉交通数据中的长距离时空动态性。同时，这些预测模型的高计算成本也限制了它们在实际业务场景中的应用。本研究提出了一种具有高预测精度和高计算效率的自监督时空瓶颈注意力网络（SSTBAN）。本文首次将自监督学习方法引入时空交通数据预测领域，显著提高了预测模型的泛化性和稳健性。此外，还设计了一种时空瓶颈注意力机制，可以以较低的计算成本高效地编码交通数据的全局时空动态性。在三个公开数据集上的实验结果充分证明了所提出方法的优越性。

![图10 SSTBAN](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919144719.png)

### 11. PriSTI: A Conditional Diffusion Framework for Spatiotemporal Imputation

**作者：**Mingzhe Liu (Beihang University)*; Han Huang (Beihang University); Hao Feng (BUAA); Leilei Sun (Beihang Univerisity); Bowen Du (Beihang Univeristy); Yanjie Fu (University of Central Florida)

**论文链接：**https://ieeexplore.ieee.org/document/10184808

**代码：**https://github.com/LMZZML/PriSTI

**关键词：**扩散模型，时空插补

**一句话概括**：本文提出了一种基于diffusion model的时空数据插补模型，通过提取条件特征和地理信息来计算时空全局相关性，从而捕捉时空依赖关系。相比于现有的自回归插补模型，提出的方法能够更准确地填充缺失值。

**论文简介：**时空数据挖掘在空气质量监测、人流模型建模和气候预测等方面发挥着重要作用。然而，在现实世界中收集的原始时空数据通常因传感器故障或传输丢失而不完整。时空插补旨在根据观察到的值和它们的潜在时空依赖性来填补缺失值。先前的主流模型是自回归地插补缺失值，存在误差累积问题。扩散概率模型可以基于可观测值插补缺失值，避免从不准确的历史插补中推断缺失值。然而，当应用扩散模型进行时空插补时，条件信息的构建和利用是不可避免的挑战。为了解决以上问题，本文提出了一个增强先验建模的条件扩散框架，即PriSTI，用于时空插补。PriSTI框架首先提供一个条件特征提取模块，从条件信息中提取粗糙但有效的时空依赖关系，作为全局上下文先验。然后，一个噪声估计模块通过条件特征计算的时空注意权重将随机噪声转换为真实值，同时考虑了地理关系。PriSTI在不同实际时空数据的各种缺失模式中表现优越，并有效处理高缺失率和传感器故障等情况。

![图11 PriSTI](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921151641.png)

### 12. Dynamic Hypergraph Structure Learning for Traffic Flow Forecasting

**作者：**Yusheng Zhao (Peking University)*; Xiao Luo (UCLA); Wei Ju (Peking University); Chong Chen (Peking University); Xian-Sheng Hua (Terminus Group); Ming Zhang (Peking University）

**论文链接：**https://ieeexplore.ieee.org/document/10184800

**关键词：**交通预测，超图

**一句话概括：**本文提出了一种新的交通流量预测模型——动态超图结构学习（DyHSL）模型，通过提取超图结构和引入交互图卷积块，以捕获高阶时空关系特征。

**论文简介：**本文对交通流量预测问题进行了研究。现有采取图神经网络的方法在处理复杂交通网络数据时能力有限，其难以捕捉非两两关系，且现有方法都是采用线性聚合方式传递信息，无法捕获高阶信息。基于此，本文提出了一种新的交通流量预测模型——动态超图结构学习（DyHSL）模型。该模型能够提取超图结构用于建模交通网络中的动态信息，并从聚合节点相关的超边聚合信息来更新节点表示。此外，其引入了交互图卷积块，建立各节点的邻域交互模型以捕获高阶时空关系。该模型通过将以上两种视图整合到一个多尺度相关信息提取模块中，并采用不同尺度的时域池化来建模不同的时域模式。本文将模型在四种常用的交通流量数据集上进行了实验，结果表明本文提出的DyHSL是有效的。

![图12 DyHSL](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919192313.png)

可参考北大计算机公众号：https://mp.weixin.qq.com/s/Tlqc1X7L8TSnvQNt33dQfQ

### 13. A Lightweight Framework for Fast Trajectory Simplification. 

**作者：**Ziquan Fang (Zhejiang University); Changhao He (Zhejiang University); Lu Chen (Zhejiang University); Danlei Hu (Zhejiang University); qichen sun (zhejiang university); linsen li (zju); Yunjun Gao (Zhejiang University)*

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184900

**关键词：**轨迹简化，轨迹表示学习

**一句话概括：**轨迹简化方法可以将GPS传感器收集的大量轨迹数据减少为一组连续的线段，以解决数据存储和处理成本高昂的问题。本文提出了名为S3的Seq2Seq2Seq框架，通过可微重建学习实现了轻量级的自监督轨迹简化，显著提高了效率并保持了压缩质量。

**论文简介：**本文针对轨迹简化问题进行了研究。现有轨迹简化方法大多存在非数据驱动且依赖于人为制定规则或预定义参数、误差度量的计算成本较高和难以捕获轨迹压缩的全局移动模式等问题。为了解决上述问题，本文提出了一种新的Seq2Seq2Seq框架，简称S3。该框架由两个堆叠的端到端结构组成。通过可微重建学习，S3可实现轻量级的自监督轨迹简化。本文将S3部署到图神经网络上，以捕捉上下文感知的移动模式，并利用地理语义增强轨迹表示，其中上下文感知的距离度量用于质量评估。该框架在两个数据集、在线及离线两种场景下都取得了更好的效率和压缩质量。

![图13 Seq2Seq2Seq](https://gitee.com/bestZKS/note-pic/raw/master/img/20230920102139.png)

### 14. LHMM: A Learning Enhanced HMM Model for Cellular Trajectory Map Matching. 

**作者：**Weijie Shi (Soochow University)*; Jiajie Xu (Soochow University); Junhua Fang (Soochow University); Pingfu Chao (Soochow University); An Liu (Soochow University); Xiaofang Zhou (The Hong Kong University of Science and Technology)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184797

**一句话概括：**提出了一种名为LHMM的学习增强的HMM模型，用于解决信令轨迹地图匹配问题。通过将神经网络的知识融入到HMM框架中，该模型能够准确地匹配信令轨迹数据到道路网络，并在高定位误差下取得了高准确性和鲁棒性的结果。

**论文简介：**本文解决了基于移动通信数据的信令轨迹地图匹配（Cellular Trajectory Map-Matching, CTMM）问题。传统的地图匹配方法主要适用于GPS轨迹，不适用于CTMM任务。因此，本文提出了一种学习增强的隐马尔可夫模型（Learning-enhanced HMM, LHMM）来解决CTMM问题。该方法通过将神经网络获得的知识融入到学习概率中，减少定位误差的影响。同时，采用多关系图学习方法生成有意义的嵌入，充分保留多关系有用信息在共享空间中。设计了一种注意力神经网络作为观测概率的学习器，结合了在不同轨迹上下文中道路和基站之间的动态相关性知识。使用转移概率学习器捕捉增强的转移概率建模的隐含深层特征。最后，将学习到的观测和转移概率无缝集成到HMM中，以指导更准确的路径查找。通过对两个大规模信令数据集的广泛实验，证明了该方法在CTMM上具有高准确性和鲁棒性。

![图14 LHMM](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921094930.png)

### 15. Contrastive Trajectory Similarity Learning with Dual-Feature Attention

**作者：**Yanchuan Chang (The University of Melbourne); Jianzhong Qi (The University of Melbourne)*; Yuxuan Liang (National University of Singapore); Egemen Tanin (University of Melbourne)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184862

**代码：**https://github.com/changyanchuan/TrajCL

**一句话概括：**本文提出了一种基于对比学习的无监督轨迹相似性度量方法TrajCL

**论文介绍：**轨迹相似度度量在轨迹数据库的查询操作中充当了关键角色，对查询效率也有很大的影响。理想的测量方法应该能够在很短的时间内准确地评估任意两个轨迹之间的相似性。然而，现有的启发式度量主要基于遵循手工制定的规则逐点比较，因此在许多情况下结果质量很差或效率很低。本文提出了一种基于对比学习的轨迹建模方法TrajCL。具体来说，本文提出了四种轨迹增强方法，并提出了一种新的基于双特征自注意的轨迹主干编码器，可以同时学习轨迹的空间模式和结构模式。本文在训练的时候选用MoCo框架，并将两种不同的轨迹增强方法得到的样本作为输入的两种视图。在基于跳跃采样生成标签的相似轨迹搜索任务中，TrajCL比现有最先进的相似度度量方法具有更高的准确性和更高的计算效率。并且经过微调，即当被用作启发式度量的估计器时，TrajCL在相似轨迹搜索任务上的效果也远超最先进的监督方法。

**一句话概括：**本文提出了一种基于对比学习的无监督轨迹相似性度量方法TrajCL

**论文介绍：**轨迹相似度度量在轨迹数据库的查询操作中充当了关键角色，对查询效率也有很大的影响。理想的测量方法应该能够在很短的时间内准确地评估任意两个轨迹之间的相似性。然而，现有的启发式度量主要基于遵循手工制定的规则逐点比较，因此在许多情况下结果质量很差或效率很低。本文提出了一种基于对比学习的轨迹建模方法TrajCL。具体来说，本文提出了四种轨迹增强方法，并提出了一种新的基于双特征自注意的轨迹主干编码器，可以同时学习轨迹的空间模式和结构模式。本文在训练的时候选用MoCo框架，并将两种不同的轨迹增强方法得到的样本作为输入的两种视图。在基于跳跃采样生成标签的相似轨迹搜索任务中，TrajCL比现有最先进的相似度度量方法具有更高的准确性和更高的计算效率。并且经过微调，即当被用作启发式度量的估计器时，TrajCL在相似轨迹搜索任务上的效果也远超最先进的监督方法。

![图15 TrajCL](https://gitee.com/bestZKS/note-pic/raw/master/img/20230921151157.png)

## Industry-and-applications-track

### 16. REDE: Exploring Relay Transportation for Efficient Last-mile Delivery

**作者：**Wenjun Lyu (Rutgers Universiy)*; Haotian Wang (JD Logistic); Zhiqing Hong (Rutgers University); Guang Wang (Florida State University); Yu Yang (Lehigh University); Yunhuai Liu (Peking University); Desheng Zhang (Rutgers University)

论文链接：https://ieeexplore.ieee.org/abstract/document/10184811

**关键词：**物流最后一公里

**一句话概括：**本文讨论了如何提升最后一英里订单配送效率的问题，设计了一个名为REDE的实时中继快递员调度系统，在考虑中继和配送快递员的流动性和订单目的地分布的情况下，最小化平均中继订单交付时间。实验结果表明该方法将快递员的工作效率提高了20.13%，将快递员每天接货订单数量提升了4.51%。

**论文简介：**从配送站点到顾客指定位置的最后一公里配送由指定的快递员完成。每个快递员通常在配送站收集一个配送区域的订单，并将订单配送给顾客。然而，由于实际原因（例如市区高昂的配送站租金），配送站与配送区域之间的长距离增加了快递员的工作时间，降低了最新的最后一公里交付方案的效率。在本文中，作者通过中继运输策略解决了这个问题，其中一个中继快递员在配送站收集订单并将其派给配送快递员，配送快递员专注于相应区域的订单交付。作者设计了一个名为REDE的实时中继快递员调度系统，在考虑中继和配送快递员的流动性和订单目的地分布的情况下，最小化平均中继订单交付时间（ARODT）。首先，提出了一种感知异质性任务的路径预测算法，用于表征配送快递员的流动性。然后，设计了一种感知距离的贪心算法和一种受平均中继订单交付时间约束的交换算法，用于生成中继路线，并根据实时订单接货请求进行更新。通过在38个城市的100个配送站的真实物流数据的评估结果显示，与基准方法相比，REDE将ARODT降低了8.4%。在线A/B测试显示，与最新的实际应用方法相比，REDE将快递员的工作效率提高了20.13%，将快递员每天接货订单数量提升了4.51%。

![图16-REDE](https://gitee.com/bestZKS/note-pic/raw/master/img/20230920101018.png)

### 17. Modeling Intra- and Inter-community Information for Route and Time Prediction in Last-mile Delivery 

**作者：**Yuting Qiang (Cainiao smart logistics network, Alibaba Group)*; Haomin Wen (Beijing Jiaotong University); lixia wu (Cainiao Ltd. ); Xiaowei Mao (Beijing Jiaotong University); Fan Wu (Cainiao Network); Huaiyu Wan (Beijing Jiaotong University); Haoyuan Hu (Cainiao Network)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184761/

**关键词：**路线和时间预测

**一句话概括：**提出一种层次化的深度学习模型（I2RTP）来挖掘AOI（Area of Interest）的全局和局部信息，根据待派送包裹的经纬度以及所在的AOI来预测快递员的派送路径和包裹的送达时间。

**论文简介：**物流中的末端配送一般是指快递员将包裹从最后的中转点配送到用户家门口，是物流网络中的重要一环。准确的预测末端配送中快递员的配送路径以及包裹的到达时间既能提升消费者的用户体验也能够辅助快递员规划配送路径。已有的路径和送达时间预测的研究工作通常侧重于挖掘特定场景中的复杂信息（比如接单时间、快递员行为习惯等），因此很难通用地解决不同场景中的路径和送达时间预测问题。本文提出一种层次化的深度学习模型（I2RTP）来挖掘AOI（Area of Interest）的全局和局部信息，它根据待派送包裹的经纬度以及所在的AOI来预测快递员的派送路径和包裹的送达时间。具体来说，I2RTP既建模了不同AOI之间（Inter-Community）的相对顺序，同时也对一个AOI内包裹的相对顺序以及时间差进行建模，进而预测出完整的包裹配送顺序和时间。在真实数据集上的实验结果证明了所提出的层次化学习方法在路径和时间预测（Route And Time Prediction, RTP）上的正确性，通过与其它已有方法进行对比，验证了I2RTP模型的有效性。

![图17 I2RTP](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919194736.png)

### 18 M2G4RTP: A Multi-Level and Multi-Task Graph Model for Instant-Logistics Route and Time Joint Prediction

**作者：**Tianyue Cai (Beijing Jiaotong University)*; Huaiyu Wan (Beijing Jiaotong University); Fan Wu (Cainiao Network); Haomin Wen (Beijing Jiao University); Shengnan Guo (Beijing Jiaotong University); lixia wu (Cainiao Ltd. ); Haoyuan Hu (Cainiao Network); Youfang Lin (Beijing Jiaotong University)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184794/

**关键词：**路线和时间预测

**一句话概括：**提出了一种即时物流领域路径与时间联合预测的多层级多任务图模型。

**论文简介：**即时物流领域（如外卖配送、快递揽收）对于路线和时间预测（Route and Time Prediction, RTP）的需求愈发强烈，该预测旨在预测快递员对于待访问地点的未来路线和到达时间。准确的RTP可以极大地帮助平台，如优化订单调度或改善用户体验。尽管近年来已开展了各种解决RTP问题的工作，但现有工作仍存在以下三个局限性：i）未能考虑快递员在AOI（兴趣面，如小区、办公楼）之间的高级转移模式。ii）未能实现对路线和时间的联合预测。iii）现有大量基于树或基于序列的架构欠缺建模不同地点之间空间关系的能力。为了解决上述限制，本文提出了一个多层级多任务图模型，名为M2G4RTP，用于即时物流领域路线和时间的联合预测。具体地，本文提出了一种配备了名为GAT-e的编码模块的多层级图编码器，以捕获快递员在AOI之间的高级转移模式和在具体地点之间的低级转移模式。此外，还提出了一个多任务解码器，以完成对不同层级上路线和时间的联合预测。最后，本文设计了一种基于同方差不确定性的损失加权方法，以自适应地平衡两个任务。本文在工业规模的真实数据集上进行的大量实验，并在菜鸟网络上完成了在线部署，最终证实了本文提出的模型的优越性。

![图18 M2G4RTP](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919194709.png)

以上两篇可参考：https://mp.weixin.qq.com/s/JxtsV8YQkouQeyvquPIaEQ

### 19 Delivery Time Prediction Using Large-Scale Graph Structure Learning Based on Quantile Regression

**作者：**Lei Zhang (Shandong University)*; Xin Zhou (Nanyang Technological University); Zhiwei Zeng (Nanyang Technological University); Yiming Cao (Shandong University); Yonghui Xu (Shandong University); Mingliang Wang (Alibaba Group); xingyu wu (Alibaba Group); Yong Liu (Nanyang Technological University); Lizhen Cui (ShanDong University); Zhiqi Shen (NTU)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184659/

**关键词：**物流时效预测

**一句话概括：**提出了一种基于图结构学习的分位数回归(Graph Structure Learning-based Quantile Regression, GSL-QR)电子商务ETA预测模型

**论文简介：**电商快递的预计送达时间(ETA)是电子商务中的一个关键问题。预测通常是基于空间(发货和收货地址)、时间(支付时间)和上下文(商家)属性进行的。现有方法通常将该任务形式化为一个OD (Origin - Destination) ETA预测问题，并利用图学习的属性关系。然而，现有方法大多使用固定且人工定义的图结构，对于下游ETA任务往往不是最优的，从而导致预测结果不理想。此外，目前的ETA模型往往侧重于预测精度，而没有考虑订单履约率。这在实践中可能会导致较低的履约率，即实际交付时间比模型提供的估计时间长得多，从而加剧了用户的不良体验。针对这些问题，本文提出了一种基于图结构学习的分位数回归(Graph Structure Learning-based Quantile Regression, GSL-QR)电子商务ETA预测模型。利用图结构学习动态更新订单的时空关系图，并在下游ETA预测任务的指导下学习最优的图结构和图嵌入。

为了同时保证预测精度和订单履约率，作者在GSL-QR中设计了一种多目标分位数回归，可以找到问题的帕雷托解。为了将GSL扩展到真实场景下的大规模图上，作者设计了一种快速采样的图结构学习(FS-GSL)方法，可以显著降低图结构学习的计算复杂度。最后，作者在从阿里巴巴电商平台上采集的三个行业数据集上进行了全面的实验。实验结果表明，该模型在ETA预测精度和订单履约率方面均优于基线模型。

![图19-GSL-QR](https://gitee.com/bestZKS/note-pic/raw/master/img/20230919194019.png)

### 20 GCRL: Efficient Delivery Area Assignment for Last-mile Logistics with Group-based Cooperative Reinforcement Learning

 **作者：**Hai Wang (Southeast University)*; Shuai Wang (Southeast University); Yu Yang (Lehigh University); Desheng Zhang (Rutgers University)

**论文链接：**https://ieeexplore.ieee.org/abstract/document/10184842/

**关键词：**物流最后一公里，强化学习

**一句话概括：**本文讨论了最后一英里物流的重要性以及面临的挑战，提出了一种基于群组的协同强化学习框架（GCRL）来优化系统效率，实验证明其相较于最先进模型有着12%的效果提升。

**论文简介：**最后一英里物流是快递从中转站到顾客手中这一交付过程的最后一步。在最后一英里物流系统中，城市被划分成许多派送区域供快递员完成包裹派送任务。近年来，由于不同派送区域间物流服务需求的高度动态性，最后一英里物流在系统效率和顾客体验方面面临着巨大挑战。如何设计一个合适的机制来提升系统效率和顾客体验已成为一项重要任务。本文针对派送区域分配问题，提出了基于群组的协同强化学习（GCRL）框架来优化最后一英里物流系统。首先，本文设计了一个多层次的注意力机制，以构建一个最优的快递员分组，提供协同的揽收和派送服务。其次，本文提出了一个图生成器和基于图的策略，以表示决策依赖关系并协调快递员之间的依赖行为。最后，本文设计了一个同步训练机制，以最大化折扣回报并为每个快递员指定派送区域。以多智能体建模的方式，GCRL 注重快递员之间的协作，同时考虑系统环境和快递员的偏好。实验证明，GCRL 与最先进模型相比提升了12%。

![图20 GCRL](https://gitee.com/bestZKS/note-pic/raw/master/img/20230920101724.png)

## TKDE Poster Track

**A Survey on Modern Deep Neural Network for Traffic Prediction: Trends, Methods and Challenges (Extended Abstract).** 

作者： [David Alexander Tedjopurnomo](https://dblp.org/pid/219/9713.html), [Zhifeng Bao](https://dblp.org/pid/20/3716.html), [Baihua Zheng](https://dblp.org/pid/93/4303.html), [Farhana Murtaza Choudhury](https://dblp.org/pid/115/9072.html), [A. K. Qin](https://dblp.org/pid/343/6711.html)

链接：https://ieeexplore.ieee.org/abstract/document/10184696

关键词：交通预测综述
 **Modeling Spatial Trajectories with Attribute Representation Learning (Extended Abstract).** 

论文链接：https://ieeexplore.ieee.org/abstract/document/9112685

作者：[Meng Chen](https://dblp.org/pid/25/687-3.html), [Yan Zhao](https://dblp.org/pid/88/5320-8.html), [Yang Liu](https://dblp.org/pid/51/3710-8.html), [Xiaohui Yu](https://dblp.org/pid/51/1449-1.html), [Kai Zheng](https://dblp.org/pid/73/3928-1.html)

关键词：轨迹表示学习综述
**Spatiotemporal Activity Modeling via Hierarchical Cross-Modal Embedding : Extended Abstract.** 

作者：[Yang Liu](https://dblp.org/pid/51/3710-200.html), [Xiang Ao](https://dblp.org/pid/71/1982-1.html), [Linfeng Dong](https://dblp.org/pid/134/4260.html), [Chao Zhang](https://dblp.org/pid/94/3019-14.html), [Jin Wang](https://dblp.org/pid/92/1375-7.html), [Qing He](https://dblp.org/pid/14/3700-3.html):

论文链接：https://ieeexplore.ieee.org/document/10184623

关键词：多模态，时空活动

 **A Deep Neural Network for Crossing-City POI Recommendations : (Extended Abstract).** 

作者：[Dichao Li](https://dblp.org/pid/248/6137.html), [Zhiguo Gong](https://dblp.org/pid/95/6295.html)

论文链接：https://ieeexplore.ieee.org/document/10184561

关键词：POI推荐

 **Time-Aware Location Prediction by Convolutional Area-of-Interest Modeling and Memory-Augmented Attentive LSTM (Extended abstract).** 

作者：[Chi Harold Liu](https://dblp.org/pid/45/4723.html), [Yu Wang](https://dblp.org/pid/02/5889-115.html), [Chengzhe Piao](https://dblp.org/pid/231/2864.html), [Zipeng Dai](https://dblp.org/pid/266/6184.html), [Ye Yuan](https://dblp.org/pid/33/6315-1.html), [Guoren Wang](https://dblp.org/pid/64/146.html), [Dapeng Wu](https://dblp.org/pid/88/1600.html)

论文链接：https://ieeexplore.ieee.org/document/10184543

关键词：兴趣区域（AOI）

**Extract Human Mobility Patterns Powered by City Semantic Diagram : Extended Abstract.** 

作者：[Zhangqing Shan](https://dblp.org/pid/139/8103.html), [Weiwei Sun](https://dblp.org/pid/63/6566-8.html), [Baihua Zheng](https://dblp.org/pid/93/4303.html)

论文链接：https://ieeexplore.ieee.org/document/10184619

关键词：人类移动性



**相关链接：**

ICDE 2023 Research Track全部接收论文:[Research Papers Track](https://icde2023.ics.uci.edu/research-papers-track/)

ICDE 2023 industry-and-applications-track全部接收论文:[Industry and Applications Track](https://icde2023.ics.uci.edu/industry-and-applications-track/)

ICDE 2023 TKDE Poster Track 全部接收论文：[TKDE Poster Track](https://icde2023.ics.uci.edu/tkde-poster-track/)

[KDD 2023 时空数据相关论文](https://zhuanlan.zhihu.com/p/650189765)

[CIKM 2023 时空数据论文总结](https://zhuanlan.zhihu.com/p/655169678)

[AAAI 2023时空数据学习相关论文汇总](https://mp.weixin.qq.com/s/pAiYMnekcDc_pcI7YFSqYg)

[KDD 2022时空数据挖掘领域论文汇总](https://mp.weixin.qq.com/s/9mvHsUCvhMwphaLGmILzYw)