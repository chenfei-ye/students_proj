## 人脑认知加工功能的影像梯度模式识别

### 背景
要理解认知功能是如何从大脑结构中产生的，就必须量化那些离散的脑区是如何在更广阔的皮层中整合的。皮层在结构上特定的空间排列模式锚定了人脑功能的分化表达。尽管长久以来将神经信号的测量(例如从功能性磁共振成像，fMRI)与认知联系起来的研究方法都集中在确定离散脑区和模块及其具体的功能角色，但最近的概念和方法论的发展才提高了数据和方法，以允许**将大规模的大脑功能映射到低维流形表征（manifold representations），也称为梯度（gradients）**。利用非线性流行学习等方法进行网络嵌入（network embedding），能够刻画个体脑网络梯度，从而在低维空间对脑网络的空间组织进行表达。最近研究发现，人脑中存在一个感觉运动脑区到跨模态脑区之间的[核心梯度](https://zhuanlan.zhihu.com/p/192635016)，一个脑区在这个核心梯度组织形式中的位置可以直接反映这个脑区的微观结构、遗传特征、连接和功能作用。以**梯度**描述全脑组织原则的方式，已经为皮层模式如何与皮层动态和高水平认知相关提供了深入洞见。

### 目的
本课题以基于MRI影像的人脑连接组梯度为研究对象，提出个体水平的人脑连接组梯度定量描述指标，研究人脑梯度分布与认知行为功能的关系。

### 准备工作
1. 理解MRI影像及脑连接组基础概念，[部分参考](https://github.com/chenfei-ye/students_proj)。
2. 熟练掌握[brainspace](https://brainspace.readthedocs.io/en/latest/)计算流程（推荐python版本），并深入理解脑连接组梯度的计算本质。
3. 基于[预处理后的HCP脑功能网络数据](https://github.com/chenfei-ye/students_proj#hcp%E6%95%B0%E6%8D%AE)生成脑功能连接梯度，以及可视化。
4. 文献阅读（粗体为重点）
- Margulies DS, Ghosh SS, Goulas A, Falkiewicz M, Huntenburg JM, Langs G, Bezgin G, Eickhoff SB, Castellanos FX, Petrides M, Jefferies E, Smallwood J. Situating the default-mode network along a principal gradient of macroscale cortical organization. Proc Natl Acad Sci U S A. 2016 Nov 1;113(44):12574-12579. doi: 10.1073/pnas.1608282113. Epub 2016 Oct 18. PMID: 27791099; PMCID: PMC5098630.
- Bethlehem RAI, Paquola C, Seidlitz J, Ronan L, Bernhardt B, Consortium CC, Tsvetanov KA. Dispersion of functional gradients across the adult lifespan. Neuroimage. 2020 Nov 15;222:117299. doi: 10.1016/j.neuroimage.2020.117299. Epub 2020 Aug 21. PMID: 32828920; PMCID: PMC7779368.
- **Vos de Wael R, Benkarim O, Paquola C, Lariviere S, Royer J, Tavakol S, Xu T, Hong SJ, Langs G, Valk S, Misic B, Milham M, Margulies D, Smallwood J, Bernhardt BC. BrainSpace: a toolbox for the analysis of macroscale gradients in neuroimaging and connectomics datasets. Commun Biol. 2020 Mar 5;3(1):103. doi: 10.1038/s42003-020-0794-7. PMID: 32139786; PMCID: PMC7058611.**
- Ruan X, Huang X, Li Y, Kuang Z, Li M, Wei X. Dysfunction of human brain network hierarchy in Parkinson’s disease patients with freezing of gait. Parkinsonism Relat Disord. 2023 Jul;112:105446. doi: 10.1016/j.parkreldis.2023.105446. Epub 2023 May 24. PMID: 37245278.
- Vos de Wael R, Royer J, Tavakol S, Wang Y, Paquola C, Benkarim O, Eichert N, Larivière S, Xu T, Misic B, Smallwood J, Valk SL, Bernhardt BC. Structural Connectivity Gradients of the Temporal Lobe Serve as Multiscale Axes of Brain Organization and Cortical Evolution. Cereb Cortex. 2021 Oct 1;31(11):5151-5164. doi: 10.1093/cercor/bhab149. PMID: 34148082; PMCID: PMC8491677.
- **Xia Y, Xia M, Liu J, Liao X, Lei T, Liang X, Zhao T, Shi Z, Sun L, Chen X, Men W, Wang Y, Pan Z, Luo J, Peng S, Chen M, Hao L, Tan S, Gao JH, Qin S, Gong G, Tao S, Dong Q, He Y. Development of functional connectome gradients during childhood and adolescence. Sci Bull (Beijing). 2022 May 30;67(10):1049-1061. doi: 10.1016/j.scib.2022.01.002. Epub 2022 Jan 10. PMID: 36546249.**
- **Hong SJ, Xu T, Nikolaidis A, Smallwood J, Margulies DS, Bernhardt B, Vogelstein J, Milham MP. Toward a connectivity gradient-based framework for reproducible biomarker discovery. Neuroimage. 2020 Dec;223:117322. doi: 10.1016/j.neuroimage.2020.117322. Epub 2020 Sep 1. PMID: 32882388.**

### 研究内容
1. 探索总结人脑结构网络和功能网络的主要梯度分布特点；提出个体水平的人脑连接组梯度定量描述指标^[如explanation ratio, gradient range, gradient variation, gradient dispersion, 参考文献PMID: 36546249]；
2. 研究不同脑图谱分区^[如AAL atlas, schaefer atlas等]以及不同梯度分析参数^[如embedding approaches, similarity metrics等]对人脑网络梯度的影响规律；
3. 研究人脑梯度分布与多维度认知行为功能^[如视觉加工、持续注意、短时记忆、流体智力等]的关系，揭示个体间认知行为水平差异下的脑功能连接梯度分布模式变异规律，在个体水平完成基于脑网络梯度特征的认知行为预测。

### 技术指标
1. 提出一套脑功能连接梯度的稳定计算流程，其中在健康成年人群中的脑连接梯度稳定性指标ICC不低于90%^[Reliability evaluation across different time-series lengths and across different network sparsity thresholds, see reference PMID: 32882388]。
2. 发现与脑功能连接梯度具有统计显著性相关且相关系数>0.3的认知行为功能表型不少于2种。

### 研究路线
1. 数据优先使用[预处理后的HCP脑功能网络数据](https://github.com/chenfei-ye/students_proj#hcp%E6%95%B0%E6%8D%AE)。
2. 研究内容1可重点参考文献PMID: 36546249，重点是实现梯度构建及不同梯度指标的计算。注意个体水平的梯度必须进行[梯度对齐](https://brainspace.readthedocs.io/en/latest/python_doc/auto_examples/plot_tutorial2.html)。
3. 研究内容2可重点参考文献PMID: 32882388，重点是多种变量环境下的sensitivity analysis。
4. 研究内容3可利用单变量统计相关性分析或典型相关分析，预测部分的方法可参考文献^[https://pubmed.ncbi.nlm.nih.gov/36534603/]。

