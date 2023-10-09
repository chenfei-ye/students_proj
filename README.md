

# 人脑连接组分析-课题管理


## 背景
* [磁共振影像](#磁共振影像)
* [人脑连接组](#人脑连接组)
* [影像公开数据](#影像公开数据)
* [课题管理](#课题管理)

## 磁共振影像
### 极简版介绍
磁共振成像系统基本原理是利用人体内水分子中的原子核（主要是氢质子）在强磁场中的磁共振信号经重建进行组织或器官的成像。

**优点：**
1.MRI对人体没有电离辐射损伤;
2.MRI能获得原生三维断面成像而无需重建就可获得多方位的图像;
3.软组织结构显示清晰，对中枢神经系统的检查优于CT。
4.多序列成像（所谓多模态），为明确病变性质提供更丰富的影像信息。

[成像理论科普-资料1](https://zhuanlan.zhihu.com/p/82072660)，了解即可。

### MRI模态的基本概念
-   结构磁共振影像（sMRI, structural MRI），提供大脑的组织结构信息，如灰质、白质、脑脊液。脑解剖分区及形态测量分析中，通常需要利用sMRI模态对应扫描序列是T1-weighted三维图像；
-   弥散磁共振成像（dMRI, diffusion MRI），通过计量人体组织内水分子随机运动的特性来追踪大脑白质纤维并反映其解剖连接性。dMRI最常见的扫描protocol是DTI，其它protocol包括DKI、NODDI等；
-   功能磁共振影像（fMRI, functional MRI），基于血氧水平依赖性信号，反映大脑执行某种任务（task-fMRI）或者静息态(rs-fMRI)时，对应脑区的神经元功能活动。其理论基础是血氧水平依赖（BOLD），因此fMRI脑功能信号常称作BOLD信号。
![multimodal.png](resources/multimodal.png)


## 人脑连接组
### 人脑连接与脑网络
人脑约1000亿个神经元和千亿级神经突触连接可以用多种数学模型以复杂矩阵的方式表示。其中一种模型是把空间上分离的且周期性放电的神经元比喻成众多的振荡器。在微观-介观-宏观层面上，人脑连接组用节点和连接边组成了网络结构，通过以环路触发的瞬时激活/抑制(即协调同步)的方式实现动态地聚集协作。需要强调的是：基于MRI的人脑连接组局限在宏观层面（空间尺度）。

大脑功能的实现依赖于不同功能的大脑系统之间的有效沟通。因此连接组领域的首要目标是了解连接组的网络组织与大脑神经处理和大脑功能的能力之间的关系。同时，它也拥有一个强大的工具集来检测连接组如何改变可能会导致疾病中的大脑功能障碍。

在分析人脑连接组的构成时，脑网络被描述成一系列的节点（脑区或神经元集群）和节点之间的连边（结构或功能连接）。人脑连接组有两个基本属性：不同功能的脑区（包括认知、感觉运动整合、辨识和行为）彼此分隔（称为segregation）；不同功能区通过神经元和区域间连接将功能整合（称为integration）。

### 什么是连接组学
构成人类大脑的复杂脑网络连接被称为**脑连接组（human connectome）**。连接组是大脑皮层和皮层下结构（统称为灰质）之间的白质，这些连接就像电线一样，在大脑的功能区之间传递信息。所有独立连接都携带着来自不同且高度复杂的处理单元的数据。

“连接组学”一词源于 “基因组学”，即利用大数据来研究生物体的遗传学。英文的 Connectomics（连接组学）借用了“-omics（组学）”的后缀，因为它采用了类似的方法：大数据分析海量数据集，用于构建人类连接组数字化图谱。

### 人脑连接组计划
在 2009 年，人脑连接组计划 (HCP) 开展了为期五年的工作，以数字化方式绘制人类大脑的结构和功能神经连接。这个初始耗资 3850 万美元的项目始于美国国立卫生研究院的蓝图大挑战基金，并联合了世界顶级神经科学机构。该公开数据库目前被试数约1200人，包括结构MRI、静息态MRI、任务态fMRI、MEG等数据模态，其他数据还包括人口统计学数据、神经心理学数据、基因数据。


## 影像公开数据
### HCP数据
人口学和行为学基础信息：
- /data/unrestricted_HCP_behavior_data.csv: 被试的人口学和行为学基础信息，来自HCP官网
- /data/restricted_HCP_behavior_data.mat: 受限的行为学特征（作为基础信息的补充，来自文章[PMID: 33615091](https://pubmed.ncbi.nlm.nih.gov/33615091/)）
- /data/HCP_S1200_DataDictionary.xlsx: 被试的人口学和行为学变量解释，来自HCP官网
- 其中认知功能评分包含以下几类：
-- Episodic Memory
-- Executive Function/Cognitive Flexibility
-- Fluid Intelligence
-- Language
-- Processing Speed
-- Self-regulation/Impulsivity
-- Spatial Orientation
-- Sustained Attention
-- Working Memory
-- Composite总分

部分公开的脑连接组资源：
1. 来自[Fallon2020文章](https://pubmed.ncbi.nlm.nih.gov/33615091/)共享的脑连接组数据，[点此下载](https://zenodo.org/record/4643074)。这组HCP数据**只公开了其中100个人**，其中包含[FreeSurfer Desikan-Killiany皮层图谱](https://surfer.nmr.mgh.harvard.edu/ftp/articles/desikan06-parcellation.pdf)，以及[HCPMMP1 Glasser360皮层图谱](https://figshare.com/articles/dataset/HCP-MMP1_0_projected_on_fsaverage/3498446/2)分区下对应的脑结构网络和静息态脑功能网络。这部分数据由于样本量不够大，一般用于方法验证。以下是[Fallon2020脑连接组](https://zenodo.org/record/4643074)的部分数据说明：
- connectome/aparc_acpc_connectome_data.mat: Desikan-Killiany皮层图谱对应的脑网络，其中`SIFT2_den`对应脑结构网络，`standard_length`对应脑区节点之间的距离。
- connectome/HCPMMP1_acpc_connectome_data.mat: HCPMMP皮层图谱对应的脑网络，其中`SIFT2_den`对应脑结构网络，`standard_length`对应脑区节点之间的距离。
- rsfMRI/cfg.mat：其中`roiTS`代表BOLD时序信号，可用于构建脑功能网络 

2. 来自[Cheng2019文章](https://doi.org/10.7554/eLife.40765)共享的脑连接组数据，[点此下载](https://doi.org/10.5061/dryad.736t01r)。这组HCP数据公开了其中**831个人的脑功能网络**，图谱采用[AAL120全脑图谱](https://www.sciencedirect.com/science/article/pii/S1053811919307803)。


## 课题管理
1. [人脑认知加工功能的影像梯度模式识别](resources/brain_gradients.md)
2. 人脑影像功能动态分析计算方法
3. 神经调控下的脑影像状态切换机制
4. 神经系统疾病的脑活动时空动态异常表征方法研究
5. 神经调控下的脑影像标志物挖掘








