---
title: TOGAF ADM阶段H：架构变更管理
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-h, change-management, value-realization]
---

# TOGAF ADM阶段H：架构变更管理

> 证据范围：第12章，raw 页132–142；状态：`single-source`。

## 摘要(Summary)

阶段 H 让已部署架构保持动态和有价值。它建立 [[value-realization(价值实现)]] 过程，持续监测业务、技术、服务质量、资产、连续性和企业架构能力成熟度，比较实际绩效与预期业务价值，并把问题转化为受治理的变更需求。

[[architecture-change-management(架构变更管理)]] 的核心决策是：当前变化只需维护、需要局部重新架构，还是应启动新的 ADM 循环。标准将变化概括为简化、增量和重新架构三类，并强调判断应回到业务价值、影响范围、风险、符合性和豁免条件，而不是追求无业务依据的“渐进完美”。

![阶段H架构变更管理](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00132_img001.png)

## 目的和目标

- 维持架构开发循环和治理框架。
- 确保企业架构能力持续满足当前需求。
- 使架构在部署后继续实现原定业务价值。

## 关键输入

已部署架构、路线图、架构合同、合规评估、实施迁移计划、绩效结果，以及来自业务、技术、标准、成本和经验教训的变更请求。

## 核心步骤

1. 建立价值实现过程并影响业务项目使用架构成果。
2. 部署监测工具，跟踪业务/技术变化、价值、能力成熟度和服务质量。
3. 管理风险并分析实际架构绩效和差距。
4. 形成达到绩效目标所需的变更要求。
5. 由架构委员会决定变更、豁免和治理处理方式。
6. 必要时提出新的架构工作请求并启动下一循环。

## 技术、关键决策和跨阶段依赖

- 技术：绩效和价值监测、业务及技术趋势分析、风险管理、差距复核、变更影响分析和变化分类。
- 关键决策：变化由维护、增量重新架构还是新 ADM 循环处理，何时给予豁免，以及哪些能力、原则或框架需要更新。
- 跨阶段依赖：本阶段接收阶段 G 的新基线、合规结果和运行反馈；变更请求通过需求管理回到受影响阶段，能力问题则反馈预备阶段。

## 主要输出

- 维护性架构更新、框架和原则更新。
- 更新后的合同和合规评估。
- 对重大变化的新架构工作请求。

## 关键主张(Key Claims)

1. 架构变更管理的目标是确保架构实现原定业务价值，而不仅是保持文档最新。[原文，§12.5，raw 页137](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 业务增长、衰退、技术变化和解决方案运行经验都可能驱动变化，战略自上而下与运营自下而上的请求必须统一治理。[原文，§12.5.1，raw 页138–140](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 简化变更通常降低投资，增量变更从既有投资获得更多价值，重新架构则增加投资以创造新价值。[原文，§12.5.2，raw 页140–141](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 影响多个利益相关者或业务战略的变化更可能需要重新进入 ADM；局部、可豁免的变化更可能通过维护处理。[原文，§12.5.3，raw 页141–142](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[architecture-change-management(架构变更管理)]]
- [[value-realization(价值实现)]]与[[business-value(业务价值)]]
- [[architecture-governance(架构治理)]]
- [[architecture-development-cycle(架构开发周期)]]
- [[baseline-architecture(基线架构)]]

## 重要引文(Notable Quotes)

> “Usage of the Enterprise Architecture is the most important part of the architecture development cycle.” — §12.5，raw 页137

## 局限／偏见(Limitations / Bias)

原文给出的维护/重设计判断是指导性启发式，不是机械规则；不同组织的风险承受度和治理成熟度会改变阈值。
