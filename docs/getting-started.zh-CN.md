# NeuroAI 中文入门说明

[返回项目导航](../README.md)

这份清单围绕一个问题组织：怎样用神经科学和人工智能共同研究智能？英文 README 是项目导航；资源条目按用途放在四个目录中。本文帮助你选择起点，并说明阅读和实践时应关注什么。

- [learn：学习入门](../learn/README.md)收录综述、基础文章、课程和教程。
- [research：研究方向](../research/README.md)收录脑与模型比较、学习规则、记忆与决策相关论文。
- [practice：动手实践](../practice/README.md)收录工具、任务环境、数据集和评测基准。
- [community：相关资源](../community/README.md)收录相关资源清单。

## 从哪个方向开始

| 你想回答的问题 | 建议入口 | 第一个可完成的成果 |
| --- | --- | --- |
| NeuroAI 研究什么？ | [综述与基础](../learn/README.md#reviews-and-foundations)中的 Hassabis、Zador 两篇文章 | 各用一段话说明：论文讨论了哪些已有工作，又提出了哪些未来方向。 |
| 人工网络能解释脑活动吗？ | [脑与模型的比较](../research/README.md#comparing-brains-and-models)中的 RSA、Yamins，以及 [Brain-Score](../practice/README.md#benchmarks) | 选择一个评测，写清输入、预测对象、训练与测试划分和评价指标。 |
| 大脑的学习方式能启发算法吗？ | [学习规则与预测编码](../research/README.md#learning-rules-and-predictive-coding) | 比较两种学习规则需要哪些局部信息、反馈连接和训练条件。 |
| 网络怎样表现出记忆和决策？ | Yang 和 Wang 的 primer、[记忆与规划](../research/README.md#memory-planning-and-decision-making)、[NeuroGym](../practice/README.md#tools-and-environments) | 运行一个官方任务示例，描述观察、动作、反馈和网络状态分别是什么。 |

## 建议的学习顺序

1. **补齐必要基础。** 能阅读 Python，理解矩阵运算、概率、梯度下降和基本神经网络训练即可开始。神经科学或深度学习背景不足时，从对应的 [Neuromatch 课程](../learn/README.md#courses-and-tutorials)选学相关章节。
2. **建立领域地图。** 先读一篇综述，再浏览 Neuromatch NeuroAI 的课程目录。暂时选择视觉表征、学习规则或认知任务中的一个方向。
3. **完成一个官方教程。** 优先选择课程 notebook 或 NeuroGym 示例。记录依赖版本、使用的数据和运行命令；先确认自己理解示例的输入输出。
4. **带着具体问题读论文。** 把任务、模型、比较对象和证据分别写出来。再决定是否需要换模型、添加控制条件或使用真实神经数据。

以上顺序是本清单建议的学习路线，进度可以随你的基础调整。

## 一个小练习：比较两个模型的表征

目标：理解“两个模型的表征相似”是什么意思。

1. 从官方教程中选取同一组输入，提取两个网络或同一网络两个层的激活。
2. 分别计算输入之间的表征差异，得到两张 representational dissimilarity matrix（RDM）。
3. 确认两张矩阵的输入顺序相同，只比较上三角中不含对角线的对应元素，避免把对角线和对称重复项计入比较。记录使用的距离、相似性指标和样本数。
4. 如果进一步拟合真实神经反应，必须把拟合数据与评测数据分开，并记录重复测量可靠性或噪声上限的处理方式。

前两步只比较人工模型。引入脑数据后，结果才涉及模型与脑活动的对应；即使对应良好，也仍需额外实验来检验具体机制。方法入口见 [RSA 原始论文](../research/README.md#comparing-brains-and-models)。这是一项练习建议，本仓库没有声称已运行该实验。

## 阅读时分清四种内容

- **综述或观点：** 作者整理了什么证据，提出了什么研究议程？
- **数学结果：** 结论依赖哪些假设，适用于哪些模型？
- **计算实验：** 算法在哪个任务、数据集和比较条件下有效？
- **神经或行为证据：** 记录了什么生物信号，观察到什么关系，是否进行了干预？

例如，预测编码学习规则在特定条件下近似反向传播，是关于算法关系的结果；判断大脑是否使用该规则，还需要神经科学证据。

## 常用术语

| 英文 | 中文 | 阅读提示 |
| --- | --- | --- |
| Encoding model | 编码模型 | 从刺激或任务变量预测脑活动。 |
| Decoding model | 解码模型 | 从脑活动预测刺激、动作或其他变量。 |
| Representational similarity analysis | 表征相似性分析 | 比较不同系统对同一组条件的表征关系。 |
| Credit assignment | 信用分配 | 确定哪些神经元或连接应为误差负责。 |
| Predictive coding | 预测编码 | 用预测及其误差描述信息处理的一类模型。 |
| Meta-learning | 元学习 | 从一组任务中学习如何适应新的任务。 |
| Spiking neural network | 脉冲神经网络 | 以离散脉冲事件描述神经元输出的网络。 |

## 选择工具和数据时

Neural Latents Benchmark 的在线 EvalAI 提交已于 2026 年 1 月关闭，但其官网提供本地评测说明。PsychRNN 的文档测试环境较旧，安装前应检查兼容性。Natural Scenes Dataset 需要数据访问协议。具体入口与说明见 practice 目录的[工具](../practice/README.md#tools-and-environments)、[数据](../practice/README.md#datasets)和[基准](../practice/README.md#benchmarks)部分。

发现错误、失效链接或合适的新资源时，请按[贡献说明](../CONTRIBUTING.md)提交。
