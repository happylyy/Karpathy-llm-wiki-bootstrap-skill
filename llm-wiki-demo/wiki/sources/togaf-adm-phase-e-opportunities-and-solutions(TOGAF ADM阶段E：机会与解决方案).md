---
title: TOGAF ADM阶段E：机会与解决方案
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-e, roadmap, work-packages]
---

# TOGAF ADM阶段E：机会与解决方案

> 证据范围：第9章，raw 页106–116；状态：`single-source`。

## 摘要(Summary)

阶段 E 是从架构设计转向交付规划的转折点。它汇总阶段 B–D 的差距、需求和候选路线图组件，识别能够解决差距的 [[solution-building-block(解决方案构建块)]]，处理跨域依赖及互操作冲突，再把相关活动组合成 [[work-package(工作包)]]、项目和投资组合。

当目标不能一次实现时，本阶段定义能够产生可度量业务价值的 [[transition-architecture(过渡架构)]]。这些过渡状态和工作包被放入初版 [[architecture-roadmap(架构路线图)]]，并形成官方复合产物 “Implementation and Migration Plan”的草案。在概念层，本 Wiki 将其分析为 [[implementation-plan(实施计划)]] 和 [[migration-plan(迁移计划)]] 两个相互关联但职责不同的概念。

![阶段E机会与解决方案](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00106_img001.png)

## 目的和目标

- 汇总四域差距，生成首个完整架构路线图草案。
- 判断是否需要增量交付，并定义能持续产生价值的过渡架构。
- 以 ABB 为需求边界，确定实现目标架构的总体 SBB。

## 关键输入

四域架构和差距结果、需求、候选路线图组件、企业变革和规划方法、转型准备度、产品信息及各类治理框架。

## 核心步骤

1. 评估组织变革属性、文化、技能和实施约束。
2. 汇总业务、数据、应用、技术差距以及候选解决方案和依赖。
3. 合并跨业务职能需求及互操作需求，解决构建块冲突。
4. 验证依赖、转型准备度和风险。
5. 选择绿地、革命式或演进式实施策略。
6. 组合主要工作包并映射到项目、投资组合和能力增量。
7. 识别过渡架构，形成路线图和实施迁移计划草案。

## 技术、关键决策和跨阶段依赖

- 技术：实施因素评估及推演矩阵、跨域差距合并、依赖分析、转型准备度和风险评估、SBB 识别、工作包分组及过渡架构建模。
- 关键决策：采用绿地、革命式还是演进式策略，哪些差距合并为工作包，由哪些 SBB 实现，以及需要哪些过渡状态。
- 跨阶段依赖：本阶段综合阶段 B–D 的架构、差距和候选路线图组件；路线图、工作包和计划草案交给阶段 F 排序与定稿。

## 主要输出

- 更新后的架构定义和需求规格。
- 差距、解决方案和依赖的综合评估。
- 工作包组合、SBB、实施因素和风险。
- 过渡架构及初版架构路线图。
- Implementation and Migration Plan 草案及实施迁移策略。

## 关键主张(Key Claims)

1. 阶段 E 必须把四域差距放进同一依赖视图，否则局部解决方案可能制造跨域冲突。[原文，§9.3.3–9.3.6，raw 页109–111](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. ABB 表达所需功能，SBB 表达总体实现；一个 SBB 可以解决多个相关差距和 ABB。[原文，§9.1、§9.3.3，raw 页106、109–110](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 工作包是依据依赖、实施因素和战略方法组合的逻辑变更单元，不等同于单个项目。[原文，§9.3.9，raw 页112](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 过渡架构必须表示可实现、可测量且具有业务价值的中间状态。[原文，§9.3.10，raw 页112](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
5. 路线图描述从基线到目标的时间演进；实施迁移计划则描述实现路线图所需的活动、项目和资源。[原文，§9.3.11、§9.5，raw 页112–116](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[architecture-building-block(架构构建块)]]与[[solution-building-block(解决方案构建块)]]
- [[gap-analysis(差距分析)]]
- [[work-package(工作包)]]
- [[transition-architecture(过渡架构)]]
- [[architecture-roadmap(架构路线图)]]
- [[implementation-plan(实施计划)]]与[[migration-plan(迁移计划)]]

## 重要引文(Notable Quotes)

> “The key is to focus on the final target while realizing incremental business value.” — §9.5，raw 页115

## 局限／偏见(Limitations / Bias)

官方文本将 Implementation and Migration Plan 作为一个复合产物；本 Wiki 的概念拆分用于澄清“如何实施”和“如何迁移”的不同分析责任，不主张改变官方产物名称。
