---
title: TOGAF ADM阶段B：业务架构
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-b, business-architecture]
---

# TOGAF ADM阶段B：业务架构

> 证据范围：第4章，raw 页56–71；状态：`single-source`。

## 摘要(Summary)

阶段 B 开发能够实现 [[architecture-vision(架构愿景)]] 的 [[business-architecture(业务架构)]]。它不只描述组织结构或流程，而是综合业务能力、端到端价值交付、关键信息、组织关系、战略、产品、政策、计划和利益相关者，解释企业需要如何运作。

阶段采用可复用的域架构模式：选择参考模型、[[architecture-viewpoint(架构视点)]]和工具，建立 [[baseline-architecture(基线架构)]] 与 [[target-architecture(目标架构)]]，执行 [[gap-analysis(差距分析)]]，形成候选路线图组件，评估跨架构和跨项目影响，完成利益相关者审查并更新架构定义文档。

![阶段B业务架构](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00056_img001.png)

## 目的和目标

- 描述企业为实现业务目标和战略驱动因素所需的目标业务运作方式。
- 根据业务架构基线与目标之间的差距提出候选 [[architecture-roadmap(架构路线图)]] 组件。

## 关键输入

架构愿景、已批准的工作说明、能力评估、业务原则和驱动因素、企业连续统一体、架构存储库、高层需求及既有基线/目标描述。

## 核心步骤

1. 选择参考模型、视点和建模工具，并确定所需目录、矩阵、图和需求类型。
2. 只以支持目标决策所必需的详细程度建立基线业务架构。
3. 建立目标业务架构，必要时比较多个替代方案。
4. 验证模型一致性和需求完整性，执行差距及权衡分析。
5. 将差距转化为候选业务路线图组件。
6. 评估架构景观和其他项目的双向影响。
7. 经正式审查后完成构建块、需求可追溯性和架构定义文档。

## 方法重点

- [[business-capability(业务能力)]]映射说明企业“能够做什么”，且独立于当前组织和系统。
- [[value-stream(价值流)]]说明企业“如何为特定利益相关者创造价值”，其阶段依赖业务能力。
- 组织图说明哪些业务单元、伙伴或第三方拥有或使用能力并参与价值流。
- 信息图从产品、客户等业务核心信息出发，连接后续数据、应用和基础设施分析。

## 技术、关键决策和跨阶段依赖

- 技术：业务能力映射、价值流映射、组织映射、业务信息映射、业务场景、热力图、差距分析和权衡分析。
- 关键决策：基线需要多少细节、采用哪个目标方案、哪些能力和价值流差距最重要，以及哪些差距进入候选路线图。
- 跨阶段依赖：本阶段接收阶段 A 的愿景、范围和需求；其目标业务架构约束阶段 C/D，并把业务差距和路线图组件交给阶段 E。

## 主要输出

- 获批的基线业务架构和目标业务架构。
- 业务能力、价值流、组织、职能、流程、角色、服务、产品和业务数据视图。
- 业务架构差距、更新后的需求及技术影响。
- 业务架构路线图组件。

## 关键主张(Key Claims)

1. 其他架构域依赖对业务架构的理解，因此业务架构通常是详细域架构工作的起点。[原文，§4.5.1，raw 页65–66](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 只应收集足以支持当前范围内决策的信息；过度建模会浪费资源并模糊重点。[原文，§4.5.1，raw 页66](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 能力映射、价值流和组织图分别回答“做什么”“为何及如何交付价值”“由谁参与”，组合使用才能形成业务语境。[原文，§4.5.3–4.5.5，raw 页66–68](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 每个差距只有在具体业务需求中才有意义；热力图等技术用于把差距转化为后续阶段的优先级。[原文，§4.5.3–4.5.4，raw 页67](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[business-architecture(业务架构)]]
- [[business-capability(业务能力)]]与[[value-stream(价值流)]]
- [[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]]与[[gap-analysis(差距分析)]]
- [[stakeholder-concern(利益相关者关注点)]]与[[architecture-viewpoint(架构视点)]]
- [[architecture-roadmap(架构路线图)]]

## 重要引文(Notable Quotes)

> “Business Architecture relates business elements to business goals and elements of other domains.” — §4.5，raw 页65

## 局限／偏见(Limitations / Bias)

本章列出多种建模技术，但不要求全部采用；选择必须由当前利益相关者关注点、范围和决策需要驱动。
