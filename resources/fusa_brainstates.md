## 神经调控下的脑影像标志物挖掘
### 背景
聚焦超声消融手术（FUSA）是通过超声换能器将电能转变为声能，并将换能器发出的超声波聚焦于靶区组织并产生60~100℃高温，使靶区组织发生凝固性坏死，聚焦方式类似于用放大镜聚焦太阳光，通过局部定向的高温达到无创手术的目的。小型开放标签研究表明，丘脑Vim核FUSA可减轻帕金森病患者异动症和运动症状，疗效可维持1年以上。尽管FUSA优势明显，但它的治疗作用机制仍不完全清楚。

神经影像学研究，旨在将行为的变异与大脑的变化联系起来。磁共振成像（MRI）自上世纪90年代初被发现以来，已成为实现这一目标最有效的方法之一。作为一种探测全脑活动的非侵入性工具，功能磁共振成像fMRI能够研究复杂的人脑活动过程及其在不同时空域的功能整合和分离，因此基于fMRI影像的人脑连接组自动重建、分析与功能信息解码研究十分关键。

尽管FUSA优势明显，但是FUSA本身在脑连接组层面如何改变了PD患者功能网络的拓扑结构，仍不清楚。

### 目的
本课题以基于fMRI影像的人脑功能连接组为研究对象，构建表征人脑不同功能活动模式的脑状态（brain states），研究FUSA术前，以及FUSA术后随访过程中PD患者的脑动态网络机制。

### 准备工作
1. 理解MRI影像及脑连接组基础概念，[部分参考](https://github.com/chenfei-ye/students_proj)。
2. 熟练掌握脑状态计算流程，重点是隐马尔可夫（HMM）[^36367193][^hmm]。
3. 基于[预处理后的HCP脑功能网络数据](https://github.com/chenfei-ye/students_proj#hcp%E6%95%B0%E6%8D%AE)估计个体被试的脑状态。


### 研究内容
1. 基于HMM模型识别PD患者FUSA术前的脑功能活动对应的脑状态[^36367193]，探索各状态对应的脑区激活分布；
2. 针对FUSA术后的fMRI影像数据，刻画FUSA引起的脑状态特征[^metrics]随术后康复进程的纵向改变（重点参考文献[^36623929]）。
3. 利用图论理论（graph theory），探索FUSA引起的脑状态对应网络拓扑的segregation和integration变化，参考文献[^31249501]。

### 技术指标
1. 建立一个基于HMM模型的脑状态估计流程(python版本)，鉴别PD患者FUSA术后的脑状态变化，不少于3种评估指标。
2. 利用图论理论刻画FUSA引起的脑状态对应网络拓扑的segregation和integration变化，不少于4种图论指标。

### 关键点
1. 深入理解FUSA的作用机制，参考文献[^36869241][^31539464]
2. 优先使用[预处理后的HCP脑功能网络数据](https://github.com/chenfei-ye/students_proj#hcp%E6%95%B0%E6%8D%AE)进行HMM脑状态识别的尝试。
3. 可视化参考[nilearn](https://nilearn.github.io/dev/index.html)。

[^36367193]: Hussain S, Langley J, Seitz AR, Hu XP, Peters MAK. A Novel Hidden Markov Approach to Studying Dynamic Functional Connectivity States in Human Neuroimaging. Brain Connect. 2023 Apr;13(3):154-163. doi: 10.1089/brain.2022.0031. Epub 2023 Feb 16. PMID: 36367193; PMCID: PMC10079241.
[^33038538]: Park BY, Vos de Wael R, Paquola C, Larivière S, Benkarim O, Royer J, Tavakol S, Cruces RR, Li Q, Valk SL, Margulies DS, Mišić B, Bzdok D, Smallwood J, Bernhardt BC. Signal diffusion along connectome gradients and inter-hub routing differentially contribute to dynamic human brain function. Neuroimage. 2021 Jan 1;224:117429. doi: 10.1016/j.neuroimage.2020.117429. Epub 2020 Oct 7. PMID: 33038538.
[^hmm]: https://github.com/hmmlearn/hmmlearn
[^metrics]: a) frequency of occurrence (the number of times each state occurs per second), b) state duration (the average time an individual resides in each state during the scanning session) and c) fractional coverage (the proportion of time that an individual resides in the state during scanning), see ref [^36623929]
[^36623929]: Chu C, Liu S, He N, Zeng Z, Wang J, Zhang Z, Zeljic K, van der Stelt O, Sun B, Yan F, Liu C, Li D, Zhang C. Subthalamic stimulation modulates motor network in Parkinson’s disease: recover, relieve and remodel. Brain. 2023 Jul 3;146(7):2780-2791. doi: 10.1093/brain/awad004. PMID: 36623929.
[^32250724]: McCormick DA, Nestvogel DB, He BJ. Neuromodulation of Brain State and Behavior. Annu Rev Neurosci. 2020 Jul 8;43:391-415. doi: 10.1146/annurev-neuro-100219-105424. Epub 2020 Apr 6. PMID: 32250724.
[^34130192]: Yang Y, Ye C, Sun J, Liang L, Lv H, Gao L, Fang J, Ma T, Wu T. Alteration of brain structural connectivity in progression of Parkinson's disease: A connectome-wide network analysis. Neuroimage Clin. 2021;31:102715. doi: 10.1016/j.nicl.2021.102715. Epub 2021 Jun 6. PMID: 34130192; PMCID: PMC8209844.
[^36869241]: Kiani L. Ultrasound ablation treatment for PD. Nat Rev Neurol. 2023 Apr;19(4):197. doi: 10.1038/s41582-023-00797-z. PMID: 36869241.
[^31539464]: Fishman P, Lipsman N. Focused ultrasound as an evolving therapy for Parkinson's disease. Mov Disord. 2019 Sep;34(9):1241-1242. doi: 10.1002/mds.27809. PMID: 31539464.
[^31249501]: Farahani FV, Karwowski W, Lighthall NR. Application of Graph Theory for Identifying Connectivity Patterns in Human Brain Networks: A Systematic Review. Front Neurosci. 2019 Jun 6;13:585. doi: 10.3389/fnins.2019.00585. PMID: 31249501; PMCID: PMC6582769.
