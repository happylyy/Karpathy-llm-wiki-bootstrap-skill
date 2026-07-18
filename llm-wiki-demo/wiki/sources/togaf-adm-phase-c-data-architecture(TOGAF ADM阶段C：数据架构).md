---
title: TOGAF ADM阶段C：数据架构
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-c, data-architecture]
---

# TOGAF ADM阶段C：数据架构

> 证据范围：第6章，raw 页73–84；状态：`single-source`。

## 摘要(Summary)

数据架构子阶段定义支持业务架构和愿景的数据目标状态。它从业务架构及既有应用材料收集数据需求，统一数据目录和语义，建立数据与业务能力、职能、服务、访问权及应用之间的关系，再分析数据如何创建、分发、迁移、保护和归档。

本章把数据区分为静态存储、交易或 API 中的流动数据、应用边界处的使用中数据及面向公众的开放数据。数据治理不仅是技术问题，还需要组织结构、管理制度及人员技能；数据迁移则必须明确清洗、转换、质量和共同定义要求。

## 目的和目标

- 建立支持目标业务架构及愿景的 [[target-architecture(目标架构)]]。
- 从数据基线和目标的差距中识别候选路线图组件。

## 关键输入

工作说明、架构愿景、业务架构差距、数据原则、数据相关可复用构建块、参考模型、标准及业务路线图组件。

## 核心步骤

1. 选择数据参考模型、视点、工具及所需目录、矩阵和图。
2. 统一数据需求和企业数据目录，建立数据清单及实体关系。
3. 建立数据—业务—应用矩阵，暴露无人创建、无人使用或重复的数据。
4. 开发必要的基线和目标数据描述，执行差距和权衡分析。
5. 评估对业务、应用、技术架构及其他项目的影响并进行正式审查。
6. 完成数据构建块、需求可追溯性、架构定义及路线图组件。

## 技术、关键决策和跨阶段依赖

- 技术：数据目录、实体关系模型、数据—业务和数据—应用矩阵、数据生命周期分析、迁移分析、质量分析及治理评估。
- 关键决策：采用何种数据粒度和共同定义、由谁创建和管理数据、数据如何流动，以及哪些现状应保留、迁移或消除。
- 跨阶段依赖：本子阶段接收业务架构和既有应用信息；其数据责任、质量、迁移和访问约束反馈应用架构，并约束技术架构和阶段 E。

## 主要输出

- 获批的基线和目标数据架构。
- 业务数据模型、逻辑数据模型、数据管理过程模型及数据实体/业务职能矩阵。
- 数据互操作、迁移、质量和治理需求。
- 对应用和技术架构的约束及数据路线图组件。

## 关键主张(Key Claims)

1. 数据模型必须从业务服务、能力和信息需求追溯，而不能仅从既有数据库反向汇总。[原文，§6.3.1，raw 页75–78](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 数据详细程度要服从决策需要；高层概念图和现有物理模式代表不同层次，不能混作同一基线。[原文，§6.3.1.4，raw 页77–78](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 数据架构应覆盖静态、流动、使用中和开放数据，并区分数据实体、逻辑组件及物理组件。[原文，§6.5.1，raw 页81–82](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 数据迁移的目标不是简单搬运，而是让目标应用获得符合共同定义和质量要求的数据。[原文，§6.5.2.2，raw 页83](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
5. 数据治理需要结构、管理体系和人员三个维度共同到位。[原文，§6.5.2.3，raw 页83–84](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[data-architecture(数据架构)]]
- [[business-architecture(业务架构)]]与[[application-architecture(应用架构)]]
- [[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]]与[[gap-analysis(差距分析)]]
- [[architecture-building-block(架构构建块)]]
- [[architecture-roadmap(架构路线图)]]

## 重要引文(Notable Quotes)

> “A structured and comprehensive approach to data management enables the effective use of data.” — §6.5.2.1，raw 页82

## 局限／偏见(Limitations / Bias)

本章提供架构级数据结构和治理问题，不替代数据库设计、数据工程或具体法规合规方法。
