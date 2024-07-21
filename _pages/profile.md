---
layout: archive
title: "简历"
permalink: /profile/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

# 求职意向

工作技能：推理框架开发，C++，python，Git，Linux，Android，熟悉多种框架（PyTorch，TFLite，llama.cpp等）

求职意向：大模型推理，推理框架开发，高性能计算

# 教育经历

- 武汉大学，硕士，2021.09 - 2023.06
  - 电子信息学院
  - 电子信息（人工智能）
  - 高分辨率信息智能处理与应用研究组

- 武汉大学，本科，2017.09 - 2021.06
  - 电子信息学院
  - 通信工程，通信工程实验室
  - 申请并获得创新学分

# 科研成果

- Applied Sciences（SCI）：[Residual Dense Swin Transformer for Continuous-Scale Super-Resolution Algorithm](https://masteryi-0018.github.io/publication/2024-05-12)（通信作者）
- IGARSS（IEEE）：[Semi-supervised land-cover mapping based on multimodal fusion and pseudo-label](https://masteryi-0018.github.io/publication/2022-09-28)（第一作者，oral）
- 武汉大学学报（CNKI）：[基于注意力机制的复杂背景连续手语识别](https://masteryi-0018.github.io/publication/2022-11-30)（学生第二作者）
- ISBDAS（EI）：[Population and cultural disasters caused by sea level rise based on regression model](https://masteryi-0018.github.io/publication/2020-08-21)（共同第一作者）
- 实用新型专利：一种车位停车检测装置（第二作者，专利号ZL 2020 2 0773489.7）
- 软件著作权：牛备工程设备租赁平台（第一作者，登记号2021SR0589334）
- 软件著作权：AI车易停用户平台（第一作者，登记号2020SR0661990）
- 软件著作权：AI风控智能预测算法软件（学生第一作者，登记号2021SR0455619）

# 工作经历

**小米 玄戒 - 深度学习推理框架**

**支持自研芯片在AI领域的打榜能力**

2023.11 - 2024.08

自研芯片需要对外展示AI领域的性能分数，通常使用AI Benchmark作为统一的标准，为对接AI Benchmark，自研芯片需要提供多后端的推理框架，并且对接外部生态，主要包括Android NNAPI与tensorflow lite。

为对接Android NNAPI生态，开发基于AIDL接口的service，支持service自启动，接受NN runtime下发任务，将自研NPU作为自定义加速器，支持同步与异步执行；为对接tensorflow lite生态，开发基于自研芯片多后端推理框架的delegate，通过创建tflite external delegate，将子图转移至自研NPU作为自定义加速器，从而完成对网络任务的加速。

主要特性为：支持子图级别IR mapping，支持通用图优化，支持在线编译到NPU后端，支持layout转换。最终完成支持40+算子mapping到自研NPU IR，支持21个AI Benchmark网络成功运行在NPU后端，且精度符合要求。交付需求40+，代码10k+。


**基于自研芯片NPU子系统的大模型预研**

2023.02 - 2024.02

基于自研芯片NPU子系统，对外提供小米大模型推理能力，为大模型部署在NPU后端提供前期分析。主要包括：convertor部分通过添加算子，成功支持小米大模型由pytorch转换为自研NPU IR；针对大模型无法一次读入内存的问题，使用分段加载的策略，切分大模型；对于大模型推理速度慢的问题，积极跟进业内动态，对于kv-chche，投机推理，美杜莎等加速方法在NPU后端落地有一定预研工作。

基于自研芯片NPU子系统，对外提供stable diffusion模型的推理能力，为stable diffusion模型部署在NPU后端提供前期分析。通过分析竞品的模型转换，加速策略等，对stable diffusion模型计算量、参数量进行摸底与评估，为后续stable diffusion模型部署的立项和落地提供了前期支持。

# 开源项目经历

**开源推理框架MiniNN**

一个从零开始的C++推理框架MiniNN。定义了框架的IR表示，包括graph，node，tensor，支持神经网络图构建；支持运行时op和kernel的注册；支持通过flatbuffers序列化与反序列化；支持使用googletest进行单元测试，支持cmake与bazel编译。项目地址：[https://github.com/masteryi-0018/MiniNN](https://github.com/masteryi-0018/MiniNN)

**PyTorch中文文档**

翻译Deploying PyTorch Models in Production部分。针对PyTorch模型的部署，翻译了：使用 Flask 部署一个 PyTorch 模型，TorchScript简介，在C++中加载 TorchScript 模型，使用 ONNX 运行一个PyTorch模型，树莓派 4 上的实时推理等内容。项目地址：[https://github.com/masteryi-0018/pytorch-doc-zh](https://github.com/masteryi-0018/pytorch-doc-zh)

# 在校项目经历

**IEEE GRSS全球数据融合大赛**

2022.01 - 2022.03

针对基于MiniFrance拓展的数据集MiniFrance-DFC22，进行语义分割模型的训练；采用弱增强及CutMix等强增强方法对数据集进行充分处理，模型采用以SE-ResNeXt为backbone的Deeplabv3+，使用带权重的CE loss，对占比小的类别单独使用二分类模型进行融合，最终在决赛中取得第4名的成绩；项目地址：[https://github.com/masteryi-0018/SLM](https://github.com/masteryi-0018/SLM)

**基于注意力机制的复杂背景连续手语识别**

2021.04 - 2021.08

针对手语识别落地应用困难的问题，使用关键帧抽取、固定窗口裁剪以及resize等预处理，在较少计算量的同时提高最终精度，使用3D-ResNet作为encoder，LSTM作为decoder的seq2seq模型，并且结合复杂背景去除模块，提出了一种新颖的基于注意力机制与3D-CNN的连续手语识别算法；项目地址：[https://github.com/masteryi-0018/SLR](https://github.com/masteryi-0018/SLR)

**基于生成对抗网络的图像质量评价算法**

2020.12 - 2021.05

针对无参考图像质量评价结果与人眼主观感知贴合度不高的问题，受生成对抗网络在图像生成领域的启发，利用GAN进行伪参考图像的生成，其中生成器为7层的U-Net，判别器为全卷积网络，并在此基础上，使用绝对损失、SSIM损失和感知损失共同进行优化，巧妙地将NR-IQA问题转化为FR-IQA问题；作为毕业设计获得优秀本科毕业论文

**基于机器学习的方言识别系统**

2020.03 - 2020.05

作为语音信号处理课程设计，完成方言数据集制作，特征提取，多分类器交叉验证等工作；特征包括MFCC、GTCC、SDC等，分类器包括KNN、SVM、GMM、LSTM等，并且使用MATLAB开发图形化操作界面，对粤语、闽南语、长沙话、南昌话、河南话、普通话进行识别分类，综合正确率在85%以上

# 荣誉奖项

- 2022 优秀学业奖学金一等奖（10%）（2022.10）
- 2022 IEEE GRSS全球数据融合大赛第4名（2022.04）
- 武汉大学优秀学生干部（1%）、武汉大学社会活动积极分子（2%）（2022.05）
- 第七届中国“互联网+”大学生创新创业大赛广东省三等奖（2021.08）
- 第十六届“挑战杯”全国大学生课外学术科技作品竞赛广东省一等奖（2021.07）
- 第十届全国大学生电子商务“创新、创意及创业”挑战赛广东省二等奖，其中校级特等奖（2020.08）
- 2019 第七届武汉军运会优秀志愿者及先进个人（2019.10）
- 2019 武汉大学暑期社会实践二等奖及先进个人（2019.09）

# 社团和组织经历

**共青团武汉大学委员会 - 基层团建指导中心 - 副主任**

2021.07 - 2022.06

配合校团委组织办公室，面向全校各分团委、直属团总支开展基层团组织建设指导工作；工作内容涵盖未来学院、研支团、青马工程等，具体负责青马工程项目组，包括本科生青马班以及研究生青马班的选拔流程、培养方案、外出实践等活动

**电子信息学院团委 - 运营部 - 常委**

2017.09 - 2019.06

负责学院团委宣传工作，包括QQ号，微信公众号等，运营微信公众平台拥有3000+关注量，主笔的推送获得武汉大学创意推送大赛最佳创意奖；组织筹划表情包大赛、配音大赛，参与协调多项大型活动；担任电子信息学院“青年讲师团”成员

# 证书/技能及兴趣爱好

- 证书：CET-6，计算机二级，普通话证书
- 技能：c++，python，pytorch，git，linux，docker
- 兴趣爱好：长跑（武汉大学校运会男团第四名），摄影（武汉大学摄影故事大赛二等奖），尤克里里

---

> 相关链接：
- [LeetCode](https://leetcode.cn/u/masteryi-0018/)
- [CSDN](https://blog.csdn.net/qq_45510888)
- [知乎](https://www.zhihu.com/people/masteryi-0018)
- [豆瓣](https://www.douban.com/people/masteryi-0018/)
