# IJCAI 2023 时空数据论文

**Open Anomalous Trajectory Recognition via Probabilistic Metric Learning**

作者：Qiang Gao; Xiaohan Wang; Chaoran Liu; Goce Trajcevski; Li Huang; Fan Zhou

机构：西南财经大学、电子科技大学、爱荷华州立大学

论文链接：https://www.ijcai.org/proceedings/2023/0233.pdf

代码：https://github.com/ypeggy/ATROM

研究内容：轨迹异常检测、度量学习

摘要：通常，被认为异常的轨迹是偏离通常驾驶模式（交通规则制定）的轨迹。 然而，这种封闭的环境无法识别未知的异常轨迹，导致自我激励的学习范式不足。 本文研究了开放世界场景（ATRO）中的新异常轨迹识别问题，并引入了一种新的概率度量学习模型 ATROM来解决该问题。 具体来说，ATROM 除了识别已知行为之外，还可以检测未知异常行为的存在。 提出相互交互蒸馏方法，使用对比度量学习来探索有关不同行为意图的交互语义，以及概率轨迹嵌入，迫使具有不同行为的轨迹遵循不同的高斯先验。 更重要的是，ATROM 提供了一种概率度量规则，通过利用多个先验的近似来区分已知和未知的行为模式。 两个大规模轨迹数据集的实验结果证明了 ATROM 在解决已知和未知异常模式方面的优越性。

![ATROM](./IJCAI23_img/ATROM.png)

**Learning Gaussian Mixture Representations for Tensor Time Series Forecasting**

作者：Jiewen Deng; Jinliang Deng; Renhe Jiang; Xuan Song

机构：南方科技大学、悉尼科技大学、东京大学

论文链接：https://www.ijcai.org/proceedings/2023/0231.pdf

代码：https://github.com/beginner-sketch/GMRL

研究内容：时空预测，多元时间序列预测

摘要：张量时间序列（TTS）数据是一维时间序列在高维空间上的推广，在现实场景中普遍存在，特别是在涉及多源时空数据的监控系统（例如交通需求、空气污染物）中。 与近年来备受关注并取得巨大进展的时间序列或多元时间序列建模相比，张量时间序列付出的努力要少一些。 由于其高维且复杂的内部结构，正确处理张量时间序列是一项更具挑战性的任务。 本文开发了一种新颖的 TTS 预测框架，该框架旨在对时间、位置和源变量中隐含的每个异质性成分进行单独建模。 将该框架命名为 GMRL，是高斯混合表示学习的缩写。 两个真实世界 TTS 数据集的实验结果验证了方法与最先进的基线相比的优越性。



![GMRL](./IJCAI23_img/GMRL.png)

**Minimally Supervised Contextual Inference from Human Mobility: An Iterative Collaborative Distillation Framework**

作者：Jiayun Zhang; Xinyang Zhang; Dezhi Hong; Rajesh K. Gupta; Jingbo Shang

机构：加州圣地亚哥分校（UCSD），伊利诺伊大学厄巴纳-香槟分校（UIUC），亚马逊

论文链接：https://www.ijcai.org/proceedings/2023/0272.pdf

代码：https://github.com/jiayunz/STColab （这么开源是吧）

研究内容：人类移动性

摘要：移动数据中有关行程和用户的背景信息对于移动服务提供商了解其客户并改进其服务非常有价值。 现有的推理方法需要大量的标签进行训练，这在实践中很难满足。 本文研究了一种更实用但更具挑战性的设置——在最少监督的情况下使用移动数据进行上下文推理（即每个类有几个标签和大量未标记数据）。 典型的解决方案是应用遵循自训练框架的半监督方法来引导基于所有特征的模型。 然而，使用有限的标记集会给自训练带来过度拟合的高风险，从而导致性能不理想。 本文提出了一种新颖的协作蒸馏框架 STCOLAB。 它在每次迭代时按照真实标签的监督顺序训练空间和时间模块。 此外，它使用其他模态的最新训练模块产生的逻辑将知识提炼到正在训练的模块，从而相互校准两个模块并结合来自两种模态的知识。 对两个真实世界数据集的广泛实验表明，STCOLAB 比各种基线实现了更准确的上下文推理。

![STCOLAB](IJCAI23_img/STCOLAB.png)

**Towards an Integrated View of Semantic Annotation for POIs with Spatial and Textual Information**

作者：Dabin Zhang; Ronghui Xu; Weiming Huang; Kai Zhao; Meng Chen

机构：山东大学、南洋理工大学、乔治亚州立大学

论文链接：https://www.ijcai.org/proceedings/2023/0271.pdf

研究内容：兴趣点（POI）推荐

摘要：兴趣点（POI）类别从位置搜索、POI推荐等多个方面促进基于位置的服务。 然而，POI的类别往往是不完整的，并且不断产生新的POI，这就提出了对POI进行语义标注的需求，即用语义类别来标记POI。 以前的方法通常对用户的顺序签到信息进行建模，以学习 POI 特征进行注释。 然而，现实中很难获得用户的签到，尤其是对于那些新创建的POI。 在此背景下，本文提出了静态 POI 的空间文本 POI 注释 (STPA) 模型，该模型仅使用 POI 的地理位置和名称来派生 POI 类别。 具体来说，设计了一个基于 GCN 的空间编码器来对 POI 之间的空间相关性进行建模，以生成 POI 空间嵌入，并设计一个基于注意力的文本编码器来对 POI 的语义上下文进行建模，以生成 POI 文本嵌入。 最终融合两个嵌入并保留多视图相关性以进行语义注释。 利用 AMap 的 POI 数据进行了全面的实验来验证 STPA 的有效性。 实验结果表明，STPA 大大优于几个竞争基线，这证明 STPA 是一种在地图服务中注释静态 POI 中有效的方法。

![STPA](IJCAI23_img/STPA.png)

**SMARTformer: Semi-Autoregressive Transformer with Efficient Integrated Window Attention for Long Time Series Forecasting**

作者：Yiduo Li; Shiyi Qi; Zhe Li; Zhongwen Rao; Lujia Pan; Zenglin Xu

机构：哈尔滨工业大学（深圳），华为诺亚实验室，鹏城实验室

论文链接：https://www.ijcai.org/proceedings/2023/0241.pdf

研究内容：长时（long-term）序列预测

摘要：Transformer 在长时间序列预测 (LTSF) 方面的成功可归因于它们的注意力机制和非自回归 (NAR) 解码器结构，它们捕获了长程依赖性。 然而，时间序列数据还包含丰富的局部时间依赖性，这些依赖性在文献中经常被忽视并严重阻碍预测性能。 为了解决这个问题，本文提出了 SMARTformer。 SMARTformer 利用集成窗口注意力 (IWA) 和半自动回归 (SAR) 解码器从编码器和解码器的角度捕获全局和局部依赖性。 IWA 在多尺度窗口中进行局部自注意力，并在具有线性复杂性的跨窗口中进行全局注意力，以在局部和扩大的感受野中实现互补线索。 SAR 迭代生成子序列，类似于自回归 (AR) 解码，但以 NAR 方式细化整个序列。 这样，SAR 既受益于 NAR 的全局视野，又受益于 AR 的局部细节捕捉。 还引入了时间无关嵌入（TIE），它通过避免直接将位置嵌入添加到值嵌入时可能出现的各种周期的纠缠来更好地捕获局部依赖关系。 对五个基准数据集进行的广泛实验证明了 SMARTformer 相对于最先进模型的有效性。

![SMARTformer](IJCAI23_img/SMARTformer.png)

**Reinforcement Learning Approaches for Traffic Signal Control under Missing Data**

作者：Hao Mei; Junxian Li; Bin Shi; Hua Wei

机构：新泽西理工学院，西安交通大学，亚利桑那州立大学

论文链接：https://www.ijcai.org/proceedings/2023/0251.pdf

研究内容：信控优化

摘要：强化学习（RL）方法在交通信号控制（TSC）任务中的出现取得了可喜的成果。 大多数强化学习方法需要观察环境，让智能体决定哪种行动对于长期奖励来说是最佳的。 然而，在现实城市场景中，由于缺乏传感器，交通状态的缺失观测可能经常发生，这使得现有的强化学习方法不适用于缺失观测的路网。 在这项工作中，目标是在现实环境中控制交通信号，其中道路网络中的一些交叉口没有安装传感器，因此周围没有直接观察。 本文是第一个使用强化学习方法来解决现实环境中的 TSC 问题。 提出了两种解决方案：1）估算流量状态以实现自适应控制。 2) 估算状态和奖励以实现自适应控制和 RL 智能体的训练。 通过对合成和现实世界道路网络交通的广泛实验，本文提出的方法优于传统方法，并且在不同的缺失率下表现一致。 

![RLTSCMD](IJCAI23_img/RLTSCMD.png)

**InitLight: Initial Model Generation for Traffic Signal Control Using Adversarial Inverse Reinforcement Learning**

作者：Yutong Ye; Yingbo Zhou; Jiepin Ding; Ting Wang; Mingsong Chen; Xiang Lian

机构：华东师范大学，同济大学，肯特州立大学

论文链接：https://www.ijcai.org/proceedings/2023/0550.pdf

研究内容：信控优化

摘要：本文提出了一种基于对抗逆强化学习（AIRL）的交通信号控制预训练方法InitLight，能够有效生成预训练模型。该方法可仅使用多个单交叉路口数据集进行预训练，并通过智能体生成轨迹与专家轨迹进行对抗学习获得奖励函数，以还原各路口最优状态下的真实奖励。通过方法预训练可获得具有较强泛化性的预训练模型，并可迁移到其他多路口数据集上作为初始模型加速深度强化学习训练过程。

![InitLight](./IJCAI23_img/InitLight.png)

**GPLight: Grouped Multi-agent Reinforcement Learning for Large-scale Traffic Signal Control**

作者：Yilin Liu; Guiyang Luo; Quan Yuan; Jinglin Li; Lei Jin; Bo Chen; Rui Pan

机构：北京邮电大学，西安电子科技大学

论文链接：https://www.ijcai.org/proceedings/2023/0023.pdf

研究内容：信控优化

摘要：使用多智能体强化学习（MARL）方法来协调交通信号灯（CTL）已经变得越来越流行，将每个路口视为一个智能体。 然而，现有的 MARL 方法要么对待每个智能体绝对同质，即每个智能体具有相同的网络和参数，要么对待每个智能体完全异构，即每个智能体不同的网络和参数。 这在准确性和复杂性之间造成了困难的平衡，尤其是在大规模 CTL 中。 为了应对这一挑战，提出了一种名为 GPLight 的分组 MARL 方法。 首先考虑实时交通流和静态细粒度道路拓扑，挖掘智能体环境之间的相似性。 然后，提出两种损失函数来维持可学习和动态的聚类，一种使用互信息估计来获得更好的稳定性，另一种则最大化组之间的可分离性。 最后，GPLight 强制组中的智能体共享相同的网络和参数。 这种方法通过促进同一组智能体内的合作来降低复杂性，同时反映组之间的差异以确保准确性。 为了验证方法的有效性，在合成数据集和真实数据集上进行了实验，其中有多达 1,089 个交叉点。 与最先进的方法相比，实验结果证明了提出的方法的优越性，特别是在大规模 CTL 中。

![GPLighjt](IJCAI23_img/GPLighjt.png)

**(Demonstrations Track) Automated Planning for Generating and Simulating Traffic Signal Strategies**

作者：Saumya Bhatnagar; Rongge Guo; Keith McCabe; Thomas McCluskey; Francesco Percassi; Mauro Vallati

机构：赫德福特大学,Simplifai Systems

论文链接：https://www.ijcai.org/proceedings/2023/0830.pdf

研究内容：信控优化

摘要：人们对使用人工智能技术进行城市交通控制越来越感兴趣，特别关注交通信号优化。 基于模型的方法（例如规划）被证明能够实时处理意外或异常的交通状况以及常见的交通模式。 此外，此类技术所依赖的生成交通信号策略的知识模型实际上是交通的模拟模型，因此交通当局可以使用它来测试和比较不同的方法。 在这项工作中，提出了一个依赖于自动化规划来生成和模拟城市地区交通信号策略的框架。 从部署在英国柯克利斯地区主干道的传感器收集的真实世界数据进行实验，验证了该框架的有效性。

![Traffic Signal Strategies](IJCAI23_img/Traffic Signal Strategies.png)