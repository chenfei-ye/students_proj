## 神经调控下的脑影像状态切换机制
### 背景
深脑电刺激（deep brain stimulation, DBS）是帕金森病等多种神经退行疾病的主要干预手段，自上世纪80 年代开始应用于临床，2002年获得美国FDA批准，30多年来全球有超过30万人接受了该疗法。然而其临床疗效的普适性不强、刺激参数优化方式低效、长期慢性刺激容易产生不良作用。临床困境的背后是DBS作用机制不清。目前的主流观点认为DBS 不仅在局部刺激靶区发挥作用，而且在全脑范围内通过涉及运动控制的功能连接脑区产生广泛分布的脑网络效应。然而其具体机制仍未阐明，严重限制了DBS手术方案的精准优化。因此，如何研究模拟帕金森病（PD）患者人脑连接组的功能损伤和刺激响应，是DBS干预方案个体调控精准化的重要发展趋势，也成为了功能神经外科的迫切临床需求。DBS在功能失调的神经回路中放置一个电极来提供电刺激，以抑制异常的活动和驱动一个不活跃的网络。尽管DBS优势明显，但它的治疗作用机制仍不完全清楚。

神经影像学研究，旨在将行为的变异与大脑的变化联系起来。磁共振成像（MRI）自上世纪90年代初被发现以来，已成为实现这一目标最有效的方法之一。作为一种探测全脑活动的非侵入性工具，功能磁共振成像fMRI能够研究复杂的人脑活动过程及其在不同时空域的功能整合和分离，因此基于fMRI影像的人脑连接组自动重建、分析与功能信息解码研究十分关键。

DBS下的PD患者脑活动解码仍存在诸多问题亟待解决：首先，由于人脑复杂活动本身具有的高度动态特性，传统静息态fMRI测量无法捕获PD病理神经环路的全局功能活动，其解释价值十分有限，忽略了许多重要的脑状态变化信息；其次，临床PD患者往往具有多种症状且随时间波动，优化 DBS 参数配置的复杂性高，需要花费较长时间，即使患者频繁往返医院，以试错的方式不断调整，也可能无法达到最佳治疗效果。

### 目的
本课题以基于fMRI影像的人脑功能连接组为研究对象，构建表征人脑不同功能活动模式的脑状态（brain states），研究DBS作用前后PD患者的脑状态切换机制。

### 准备工作
1. 理解MRI影像及脑连接组基础概念，[部分参考](https://github.com/chenfei-ye/students_proj)。
2. 熟练掌握脑状态计算流程，重点是隐马尔可夫（HMM）[^36367193][^hmm]。
3. 基于[预处理后的HCP脑功能网络数据](https://github.com/chenfei-ye/students_proj#hcp%E6%95%B0%E6%8D%AE)估计个体被试的脑状态。


### 研究内容
1. 基于HMM模型识别健康成年人脑功能活动对应的脑状态[^36367193]，探索各状态对应的脑区激活分布；
2. 分别针对DBS术前术后研究PD患者的脑状态切换规律（重点参考文献[^36623929][^33038538]），对脑状态及状态之间的切换关系进行可视化。
3. 在PD个体水平完成基于脑状态切换规律的运动障碍康复水平预测，即构建机器学习模型，基于DBS术前和术后的脑状态参数预测术后3~6个月的运动障碍康复水平。

### 技术指标
1. 建立一个基于HMM模型的脑状态估计流程，提出不少于3种脑状态的描述性指标[^metrics]。
2. 建立一个基于脑状态切换特征的帕金森病机器学习分类模型，分类准确率不低于80%。

### 关键点
1. 深入理解DBS的作用机制，参考文献[^36623929][^32250724]
2. 数据优先使用[预处理后的HCP脑功能网络数据](https://github.com/chenfei-ye/students_proj#hcp%E6%95%B0%E6%8D%AE)进行脑状态识别的尝试。
3. 帕金森病机器学习分类建模参考文献[^34130192]。
4. 可视化参考[nilearn](https://nilearn.github.io/dev/index.html)。

[^36367193]: Hussain S, Langley J, Seitz AR, Hu XP, Peters MAK. A Novel Hidden Markov Approach to Studying Dynamic Functional Connectivity States in Human Neuroimaging. Brain Connect. 2023 Apr;13(3):154-163. doi: 10.1089/brain.2022.0031. Epub 2023 Feb 16. PMID: 36367193; PMCID: PMC10079241.
[^33038538]: Park BY, Vos de Wael R, Paquola C, Larivière S, Benkarim O, Royer J, Tavakol S, Cruces RR, Li Q, Valk SL, Margulies DS, Mišić B, Bzdok D, Smallwood J, Bernhardt BC. Signal diffusion along connectome gradients and inter-hub routing differentially contribute to dynamic human brain function. Neuroimage. 2021 Jan 1;224:117429. doi: 10.1016/j.neuroimage.2020.117429. Epub 2020 Oct 7. PMID: 33038538.
[^hmm]: https://github.com/hmmlearn/hmmlearn
[^metrics]: e.g. switching rate, proportion of time spent in each state, the average duration of a state, and fractional occupancy, see ref [^36367193]
[^36623929]: Chu C, Liu S, He N, Zeng Z, Wang J, Zhang Z, Zeljic K, van der Stelt O, Sun B, Yan F, Liu C, Li D, Zhang C. Subthalamic stimulation modulates motor network in Parkinson’s disease: recover, relieve and remodel. Brain. 2023 Jul 3;146(7):2780-2791. doi: 10.1093/brain/awad004. PMID: 36623929.
[^32250724]: McCormick DA, Nestvogel DB, He BJ. Neuromodulation of Brain State and Behavior. Annu Rev Neurosci. 2020 Jul 8;43:391-415. doi: 10.1146/annurev-neuro-100219-105424. Epub 2020 Apr 6. PMID: 32250724.
[^34130192]: Yang Y, Ye C, Sun J, Liang L, Lv H, Gao L, Fang J, Ma T, Wu T. Alteration of brain structural connectivity in progression of Parkinson's disease: A connectome-wide network analysis. Neuroimage Clin. 2021;31:102715. doi: 10.1016/j.nicl.2021.102715. Epub 2021 Jun 6. PMID: 34130192; PMCID: PMC8209844.
