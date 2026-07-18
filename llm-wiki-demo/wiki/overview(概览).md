---
title: 概览
type: overview
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [personal-research, togaf, adm, enterprise-architecture]
---

# llm-wiki-demo — 概览

> 本页面是知识库的顶层综合。当前内容来自一份官方规范，全部衍生判断均为 single-source，后续摄取新证据时应继续修订。

## 范围

这是一个个人研究知识库，用于从 PDF 文档和书籍中提炼研究问题、主张、方法和可复用概念。本轮聚焦 [[togaf-architecture-development-method(TOGAF架构开发方法)]]：把其 13 章逐章编译为中文来源页，并将跨章节稳定出现的概念连接为可维护知识图谱。

实体范围有意保持最小，只持久化来源发布者 [[the-open-group(开放群组)]] 和规范体系 [[togaf-standard(TOGAF标准)]]。来源中提到的其他文档、参考模型、框架或组织仅保留为普通文本。

## 当前状态

- 已完整摄取 C220-Part1e-Architecture Development Method.md，并建立 1 个总览来源页及 13 个章节来源页。
- 已持久化 32 个单一概念页；标题均表达一个可独立维护的概念，复合产物 Implementation and Migration Plan 在来源页保留官方名称，在概念层拆分为 [[implementation-plan(实施计划)]] 和 [[migration-plan(迁移计划)]]。
- 已建立 2 个实体页；未建立论文、独立主张、数据集、对比或综合页面。
- Wiki 当前共 52 个 Markdown 页面：48 个知识页面和 4 个维护页面。

## 方法全景

ADM 将企业架构组织为反馈闭环：预备阶段建立 [[enterprise-architecture-capability(企业架构能力)]]、原则、存储库和治理基础；阶段 A 形成 [[architecture-vision(架构愿景)]] 并取得授权；阶段 B–D 分别开发业务、数据、应用和技术架构；阶段 E/F 把差距转换为工作包、过渡状态、路线图及实施迁移安排；阶段 G 监督实现符合架构；阶段 H 监测价值和变化，并在必要时启动新的 [[architecture-development-cycle(架构开发周期)]]。

[[architecture-requirements-management(架构需求管理)]] 贯穿整个闭环。它接收每个阶段产生的新需求和变化，维持可追踪性，并将影响反馈到当前或先前阶段。因此 ADM 更适合被理解为受治理的迭代决策系统，而不是固定的阶段瀑布。

## 关键主题

### 范围、关注点及决策粒度

[[architecture-scope(架构范围)]] 通过广度、深度、时间跨度和架构域控制投入。[[stakeholder-concern(利益相关者关注点)]] 决定要回答的问题，[[architecture-viewpoint(架构视点)]] 决定如何用模型和视图回答。架构只需达到足以支持当前决策的详细程度。

### 从现状到目标

各架构域共享一套基本模式：描述 [[baseline-architecture(基线架构)]]，建立 [[target-architecture(目标架构)]]，执行 [[gap-analysis(差距分析)]]，再将差距转为候选路线图组件。大型变化可通过 [[transition-architecture(过渡架构)]] 形成可运行且有业务结果的中间状态。

### 架构规格及解决方案实现

[[architecture-building-block(架构构建块)]] 说明必须具备的能力或功能，[[solution-building-block(解决方案构建块)]] 说明由何种具体机制实现。这个边界让架构目标保持稳定，同时允许产品、服务和项目选择随实施环境变化。

### 价值驱动的交付

阶段 E/F 通过 [[architecture-roadmap(架构路线图)]]、[[work-package(工作包)]]、实施计划和迁移计划组织交付。[[business-value(业务价值)]] 支持方案及工作包排序；[[value-realization(价值实现)]] 则在部署后验证预期收益是否真正发生。

### 治理及持续演进

[[architecture-governance(架构治理)]] 控制批准、版本、合规、豁免和变更。[[architecture-change-management(架构变更管理)]] 监测运行结果和外部环境，判断变化应由维护、局部重新架构还是新一轮 ADM 处理，并把已实施状态发布为新的基线。

## 研究入口

- [[togaf-architecture-development-method(TOGAF架构开发方法)]]：方法总览和 13 章导航。
- [[concept-table]]：32 个概念的压缩定义、关系、状态和维护边界。
- [[togaf-adm-introduction(TOGAF ADM导论)]]：迭代、范围、资产复用和治理基础。
- [[togaf-adm-phase-e-opportunities-and-solutions(TOGAF ADM阶段E：机会与解决方案)]]：从跨域差距到可交付变化。
- [[togaf-adm-phase-h-architecture-change-management(TOGAF ADM阶段H：架构变更管理)]]：价值监测、变化分类和下一循环。
- [[togaf-adm-architecture-requirements-management(TOGAF ADM架构需求管理)]]：贯穿所有阶段的需求反馈机制。

## 开放问题

1. 当补充 Architecture Content、ADM Techniques 及能力治理相关官方文档后，当前 32 个概念的定义和边界会发生哪些修订？
2. 在真实组织中，哪些范围、治理和成熟度条件最能预测 ADM 产物会转化为实际业务成果？
3. 业务价值在阶段 A/F 的事前评价，如何与阶段 H 的价值实现度量建立可审计的连续证据链？
4. 数据和应用架构的往返迭代在何种依赖下最有效，何时会造成重复建模或决策延迟？
5. 如何在保持架构构建块稳定的同时，让解决方案构建块适应产品生命周期和新兴技术变化？

## 证据边界

- 当前唯一证据为 C220-Part1e-Architecture Development Method.md；概念关系来自该规范内部的跨章节综合，尚未进行外部或经验性验证。
- 本 Wiki 记录的是研究性中文编译和短引文定位，不替代原始规范；需要精确措辞时应返回 [不可变原始来源](../raw/C220-Part1e-Architecture%20Development%20Method.md)。
- 后续来源若与现有结论冲突，应更新概念状态、关系和开放问题，而不是把当前页面视为最终定论。
