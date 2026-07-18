---
title: TOGAF ADM阶段C：应用架构
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-c, application-architecture]
---

# TOGAF ADM阶段C：应用架构

> 证据范围：第7章，raw 页84–94；状态：`single-source`。

## 摘要(Summary)

应用架构子阶段定义支持业务、数据和愿景的目标应用组合。它先理解当前应用和业务需求，拆分过于复杂的应用、消除重复功能、区分逻辑与物理应用，再把应用关联到业务服务、业务能力、数据、流程、用户、地点和运营依赖。

应用架构既要描述功能分布，也要暴露集成、迁移、开发和运行约束。数据或应用侧的新发现可能触发与数据架构的短迭代；目标应用结构又会成为技术架构的平台、位置、性能和运维约束。

## 目的和目标

- 建立支持业务架构、数据架构和愿景的目标应用架构。
- 从基线和目标应用组合之间的差距形成候选路线图组件。

## 关键输入

应用原则、架构愿景、业务和数据架构差距、应用组合、可复用构建块、标准、相关需求及既有路线图组件。

## 核心步骤

1. 选择应用参考模型、视点、工具以及目录、矩阵和图。
2. 清理应用定义，拆分复杂应用、消除重复并映射逻辑/物理组件。
3. 把应用映射到业务服务、能力、数据、流程、用户和运营组织。
4. 建立基线与目标应用架构并执行差距、替代方案和权衡分析。
5. 分析对业务、数据、技术架构及其他项目的影响。
6. 完成应用构建块、需求、架构定义和路线图组件。

## 技术、关键决策和跨阶段依赖

- 技术：应用组合合理化、应用—功能矩阵、应用—数据矩阵、应用交互矩阵、逻辑/物理组件映射、差距及权衡分析。
- 关键决策：应用采用何种粒度、哪些功能重复、哪些应用保留或替换，以及集成和运行责任如何分配。
- 跨阶段依赖：本子阶段接收业务和数据需求；发现的数据责任问题反馈数据架构，其平台、位置、性能和运维约束进入阶段 D 和阶段 E。

## 主要输出

- 获批的基线和目标应用架构。
- 应用组合、应用服务、逻辑/物理组件及其关系视图。
- 应用互操作需求、数据和技术约束以及差距结果。
- 应用架构路线图组件。

## 关键主张(Key Claims)

1. 应用组合应从业务服务和能力出发验证其用途，而不是把现有应用清单直接当成目标架构。[原文，§7.3.1.1–7.3.1.3，raw 页86–89](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 应用粒度必须足以识别差距和候选工作包，同时避免不必要的设计细节。[原文，§7.3.1.1，raw 页87](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 应用与数据的关联能够揭示本地/远程数据、数据责任以及需要返回数据架构解决的问题。[原文，§7.3.1.3，raw 页88–89](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 正式审查必须识别应用变化对业务、数据和技术架构的反馈约束。[原文，§7.3.7，raw 页91](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[application-architecture(应用架构)]]
- [[business-architecture(业务架构)]]与[[data-architecture(数据架构)]]
- [[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]]与[[gap-analysis(差距分析)]]
- [[architecture-building-block(架构构建块)]]
- [[architecture-roadmap(架构路线图)]]

## 重要引文(Notable Quotes)

> “The level of granularity should be sufficient to enable identification of gaps.” — §7.3.1.1，raw 页87

## 局限／偏见(Limitations / Bias)

本章描述架构级应用组合和依赖，不替代单个应用的详细解决方案设计或软件开发方法。
