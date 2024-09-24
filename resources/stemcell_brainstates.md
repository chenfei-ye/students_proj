## 神经干细胞疗法的脑动态干预机制研究
### 背景
帕金森病（PD）是一种中枢神经系统的退行性疾病，其主要特征是黑质区多巴胺能神经元的逐渐减少。目前，对于帕金森病的主要治疗方法包括药物治疗和手术治疗。然而，这些传统的治疗手段并不是对所有患者都有效，且无法逆转神经退行性改变或增加多巴胺能神经细胞的数量。传统治疗方法仅能暂时缓解病症，并不能从根本上治愈帕金森病。因此，研究者开始探索具有强大自我更新能力和分化为神经元、星形胶质细胞及少突胶质细胞，从而改善细胞环境的神经干细胞。神经干细胞提供了一种新颖的治疗帕金森病的方法，并已经取得了初步的成功。神经干细胞在治疗中枢神经系统相关疾病方面展现出巨大潜力，能够通过以下几种方式修复神经损伤：植入的干细胞能够迁徙至受损的神经区域，替换已经死亡或受损的神经细胞，帮助修复损坏的神经网络。此外，植入的干细胞能产生大量生物活性因子和营养因子，这些因子能够激活周围的神经细胞，促进新的细胞生成和组织的重建；此外，这些细胞还能分泌促进血管新生的因子，帮助改善患处的血管系统。最后干细胞具有调控免疫的功能，能够调整免疫细胞在病理位置的数量，并通过分泌不同水平的细胞因子进行互动，发挥抗炎的保护效果。

神经影像学研究，旨在将行为的变异与大脑的变化联系起来。磁共振成像（MRI）自上世纪90年代初被发现以来，已成为实现这一目标最有效的方法之一。作为一种探测全脑活动的非侵入性工具，功能磁共振成像fMRI能够研究复杂的人脑活动过程及其在不同时空域的功能整合和分离，因此基于fMRI影像的人脑连接组自动重建、分析与功能信息解码研究十分关键。

尽管神经干细胞治疗PD体现出巨大的临床潜力，但是神经干细胞疗法如何系统改变了PD患者脑网络功能动态，仍不清楚。


### 目的
本课题以基于fMRI影像的人脑功能连接组为研究对象，构建表征人脑不同功能活动模式的脑状态（brain states），研究神经干细胞治疗作用前后PD患者的脑状态切换机制。

### 准备工作
1. 理解MRI影像及脑连接组基础概念，[部分参考](https://github.com/chenfei-ye/students_proj)。
2. 深入理解干细胞治疗的作用机制和实验流程，参考文献[^38724232]
3. 和冉晨博士具体对接，熟练掌握WEIDA脑状态计算方法和PD实验数据。
4. 基于[预处理后的HCP脑功能网络数据](https://github.com/chenfei-ye/students_proj#hcp%E6%95%B0%E6%8D%AE)估计个体被试的脑状态。


### 研究内容
1. 【对应毕业论文第三章的研究主题】：基于WEIDA模型识别健康成年人脑功能活动对应的脑状态，探索各状态对应的脑区激活分布；
2. 【对应毕业论文第四章的研究主题】：分别针对神经干细胞治疗作用前后的影像数据研究PD患者的脑状态切换规律(groupwise comparison between pre and post patients)，对脑状态及状态之间的切换关系进行可视化；建立脑状态切换指标与PD患者症状变化之间的关系（Spearman correlation analysis）。


### 技术指标
1. 建立一个基于WEIDA模型的脑状态估计流程，提出不少于3种脑状态的描述性指标[^metrics]。
2. 识别神经干细胞治疗作用前后具有显著变化的脑状态定量指标。

### 关键点
1. 深入理解LEIDA的计算方法[^28698644]，找冉晨博士请教WEIDA脑状态计算方法和LEIDA的差异。
2. 可视化参考[nilearn](https://nilearn.github.io/dev/index.html)和[enigma](https://enigma-toolbox.readthedocs.io/en/latest/pages/12.visualization/index.html)。

[^38724232]: Jiang S, Wang H, Yang C, Feng F, Xu D, Zhang M, Xie M, Cui R, Zhu Z, Jia C, Liu L, Wang L, Yang X, Yang Y, Hao H, Liu Z, Wu Z, Leng L, Li X, Sun X, Zhao X, Xu J, Zhang Y, Wan X, Bao X, Wang R. Phase 1 study of safety and preliminary efficacy of intranasal transplantation of human neural stem cells (ANGE-S003) in Parkinson's disease. J Neurol Neurosurg Psychiatry. 2024 May 9:jnnp-2023-332921. doi: 10.1136/jnnp-2023-332921. Epub ahead of print. PMID: 38724232.
[^metrics]: a) frequency of occurrence (the number of times each state occurs per second), b) state duration (the average time an individual resides in each state during the scanning session) and c) fractional coverage (the proportion of time that an individual resides in the state during scanning); d) state transition probability (the probability of transitioning from one state to another); and e) dynamic fluctuation of functional connectivity, using the HMM states as the basis of calculating the variance of functional connectivity (i.e. correlations) between each pair of regions of interest, see ref [^36623929]
[^36623929]: Chu C, Liu S, He N, Zeng Z, Wang J, Zhang Z, Zeljic K, van der Stelt O, Sun B, Yan F, Liu C, Li D, Zhang C. Subthalamic stimulation modulates motor network in Parkinson’s disease: recover, relieve and remodel. Brain. 2023 Jul 3;146(7):2780-2791. doi: 10.1093/brain/awad004. PMID: 36623929.
[^28698644]: Cabral J, Vidaurre D, Marques P, Magalhães R, Silva Moreira P, Miguel Soares J, Deco G, Sousa N, Kringelbach ML. Cognitive performance in healthy older adults relates to spontaneous switching between states of functional connectivity during rest. Sci Rep. 2017 Jul 11;7(1):5135. doi: 10.1038/s41598-017-05425-7. PMID: 28698644; PMCID: PMC5506029.
