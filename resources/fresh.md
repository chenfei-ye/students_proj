## 2024-2025大一立项-课题管理
### 总体要求
- 大一学生以项目组形式，完成一项任务（产品、设计、工艺、模型、装置、软件等），并分别在开题、中期检查、项目结题报告中，以书面或口头的形式总结表达项目计划、执行过程及结果。
- 项目负责人（即队长）要为团队明确方向、目标和任务，为每个成员确定职责和角色，在项目规划、时间管理、内外协调等方面发挥引领作用。项目团队全体成员要努力建设相互信任、互助合作、积极参与、相互激励、自我管理的团队精神。
- 项目经费专款专用，学生在预算框架下自主使用。经费使用权归项目负责人，但需经指导教师审核批准。项目经费的使用范围包括：完成项目所需要的图书费、资料费、打印费、耗材费、药品费等。



### 流程管理
- 立项：**立项报告提交deadline是11月15日**。立项报告和立项答辩的质量决定能否获得立项资助，需要特别重视。每个项目资助经费额度范围：2000-3000元。
- 立项答辩评审主要考查：①项目负责人具备的知识和能力情况，前期准备情况；②项目方案的条理性，实验设计的合理性，方法的可行性等；③选题的科学性、内容的新颖程度，研究价值；④研究目标是否明确，是否有可视化的实验过程和数据，或可量化的对比结果；⑤成员结构，跨学科、跨专业申报；⑥项目陈述和回答问题情况。
- 立项后，项目组每周认真填写大一年度项目工作记录（即周报），**周报作为各次检查和评分的依据之一**。每组队长根据组内进展和问题，整合成一份周报，最迟周日晚上10点前发我邮箱，作为项目组和指导老师的主要沟通渠道。
- 立项后，项目团队每月至少应提交一次大一年度项目工作记录（基于周报撰写）。记录内容可包括：原始数据、实验现象、发生的问题、实验的收获与思考、教师的指导意见、项目团队讨论的要点、下一步的计划等。
- 立项后，项目组每个月集中开一次线下进度会，队长预定会议室。会议时间提前跟我预约。
- 中期检查采取答辩的方式进行，专家通过查阅“中期检查报告”和听取项目负责人关于课题进展情况的汇报，对每个项目提出改进的意见和建议，给出评价成绩。2025年春季学期开展中期答辩。
- 结题验收时，各学院各自安排结题答辩时间和地点，组织专家组对申请结题的项目进行验收。大一结束时结题答辩。项目“研究报告”是《哈尔滨工业大学（深圳）大一年度项目结题报告》的重要内容，也是课题研究的主要成果。
- 每个项目组设置一个研究生领队，负责常规指导和答疑。
- 支线任务可由队长分工

### 入门基础：
- 入门工具：Linux基础指令、jupyter编程环境、docker、git、tmux等；python常用库如pandas、seaborn等；脑数据[BIDS](https://bids.neuroimaging.io/)格式
- 对于相关脑疾病医学场景的理解，如脑图谱、脑网络基础原则、疾病病理、发病规则、基于影像的疾病临床诊疗现状等
- 入门学习材料：链接：https://pan.baidu.com/s/1Dfj6kPiDZXXFICb8WZUyog?pwd=p2l5  提取码：p2l5 
- 其它资料：https://github.com/chenfei-ye，https://chenfei-ye.github.io/zh/#posts


### A组题目：脑磁图的信号处理及脑疾病辅助诊断
- 领队：杜钰
- 队长：刘晰月
- 核心数据：[omega](https://www.mcgill.ca/bic/neuroinformatics/omega)
- 核心软件：[brainstorm](https://neuroimage.usc.edu/brainstorm/)、[MNE](https://mne.tools/stable/auto_tutorials/intro/10_overview.html)、[FLUX](https://github.com/Neuronal-Oscillations/FLUX)
- 入门任务：理解MEG扫描的基本概念，以及MEG信号处理背景、理论、核心软件和方法
- 主线任务：以MEG脑活动时空动态表征模式为研究对象，研究如何利用信息理论复杂性分析来刻画人脑静息状态下功能活动的动态变异性，解析帕金森病患者的脑功能信号的可变性特征，从全脑功能活动时空复杂性分析的角度揭示帕金森病的脑机制；最终实现基于MEG的个体化PD辅助诊断AI模型，并验证模型性能。
- 支线任务1：基于核心软件的MEG信号预处理
- 支线任务2：统计分析理论和实践，如一般线性模型、T-test、ANOVA、多重比较矫正等
- 支线任务3：机器学习相关理论及实践（sklearn）

核心参考文献：
- MEG信号分析[^10.1007]
- 脑活动复杂度分析技术[^36724223]

### B组题目：静息态功能磁共振的脑网络分析及脑疾病影像学诊断
- 领队：石嘉慧
- 队长：罗湘琬
- 核心软件：[fmriprep](https://fmriprep.org/en/stable/)、[xcp-d](https://xcp-d.readthedocs.io/en/latest/index.html)、[BCT](https://github.com/aestrivex/bctpy/wiki)
- 入门任务：理解MRI成像的基本概念，及静息态功能磁共振影像（RestingState-fMRI）信号处理背景、理论、核心软件和方法
- 主线任务：以静息态fMRI人脑功能连接组的网络拓扑为研究对象，解析帕金森病（PD）、快速眼球运动睡眠期行为障碍（RBD，可视为PD早期）及帕金森叠加综合征患者（如进行性核上麻痹PSP）的脑功能网络的空间模式差异，从Yeo功能子网络拓扑的角度揭示PD病理相关的脑网络损伤机制，最终建立一个PD早期诊断（RBD和健康对照）与鉴别诊断（针对PSP和PD）的影像学AI模型，并验证模型性能。
- 支线任务1：基于核心软件的静息态fMRI信号预处理及脑网络图论分析
- 支线任务2：统计分析理论和实践，如一般线性模型、T-test、ANOVA、多重比较矫正等
- 支线任务3：机器学习相关理论及实践（sklearn）

核心参考文献：
- 脑网络分析框架[^30002509]
- 脑网络图论分析技术[^30250388]


### C组题目：任务态功能磁共振的信号处理及脑疾病机制探索
- 领队：邓子言
- 队长：孔德洋
- 核心软件：[fmriprep](https://fmriprep.org/en/stable/)、[nilearn](https://nilearn.github.io/dev/index.html)
- 入门任务：理解MRI成像的基本概念，及任务态功能磁共振影像（task-fMRI）信号处理背景、理论、核心软件和方法
- 主线任务：以任务态fMRI人脑功能图像为研究对象，解析跨诊断精神障碍在认知加工任务（Stroop task）和情绪感知任务（Face recognition task）下的脑激活表现，并解析疾病机制。
- 支线任务1：基于核心软件的任务态fMRI信号预处理
- 支线任务2：针对任务态fMRI信号的统计建模
- 支线任务3：针对任务激活脑区的功能连接模式分析（聚焦疾病异常）

核心参考文献：
- task-fMRI影像预处理[^32514178]
- 跨诊断精神障碍数据集描述[^38946958]




[^36724223]: Krohn S, von Schwanenflug N, Waschke L, Romanello A, Gell M, Garrett DD, Finke C. A spatiotemporal complexity architecture of human brain activity. Sci Adv. 2023 Feb 3;9(5):eabq3851. doi: 10.1126/sciadv.abq3851. Epub 2023 Feb 1. PMID: 36724223; PMCID: PMC9891702.
[^10.1007]: Coffman, B.A., Salisbury, D.F. (2020). MEG Methods: A Primer of Basic MEG Analysis. In: Kubicki, M., Shenton, M. (eds) Neuroimaging in Schizophrenia . Springer, Cham. https://doi.org/10.1007/978-3-030-35206-6_11
[^30002509]: Bassett DS, Zurn P, Gold JI. On the nature and use of models in network neuroscience. Nat Rev Neurosci. 2018 Sep;19(9):566-578. doi: 10.1038/s41583-018-0038-8. PMID: 30002509; PMCID: PMC6466618.
[^30250388]: Sporns O. Graph theory methods: applications in brain networks. Dialogues Clin Neurosci. 2018 Jun;20(2):111-121. doi: 10.31887/DCNS.2018.20.2/osporns. PMID: 30250388; PMCID: PMC6136126.
[^38946958]: Chopra S, Cocuzza CV, Lawhead C, Ricard JA, Labache L, Patrick LM, Kumar P, Rubenstein A, Moses J, Chen L, Blankenbaker C, Gillis B, Germine LT, Harpaz-Rote I, Yeo BT, Baker JT, Holmes AJ. The Transdiagnostic Connectome Project: a richly phenotyped open dataset for advancing the study of brain-behavior relationships in psychiatry. medRxiv [Preprint]. 2024 Jun 21:2024.06.18.24309054. doi: 10.1101/2024.06.18.24309054. PMID: 38946958; PMCID: PMC11213088.
[^32514178]: Esteban O, Ciric R, Finc K, Blair RW, Markiewicz CJ, Moodie CA, Kent JD, Goncalves M, DuPre E, Gomez DEP, Ye Z, Salo T, Valabregue R, Amlien IK, Liem F, Jacoby N, Stojić H, Cieslak M, Urchs S, Halchenko YO, Ghosh SS, De La Vega A, Yarkoni T, Wright J, Thompson WH, Poldrack RA, Gorgolewski KJ. Analysis of task-based functional MRI data preprocessed with fMRIPrep. Nat Protoc. 2020 Jul;15(7):2186-2202. doi: 10.1038/s41596-020-0327-3. Epub 2020 Jun 8. PMID: 32514178; PMCID: PMC7404612.

