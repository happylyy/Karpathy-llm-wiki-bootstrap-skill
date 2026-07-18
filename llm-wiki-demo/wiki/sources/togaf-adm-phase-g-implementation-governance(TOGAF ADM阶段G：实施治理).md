---
title: TOGAF ADM阶段G：实施治理
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-g, implementation-governance]
---

# TOGAF ADM阶段G：实施治理

> 证据范围：第11章，raw 页125–132；状态：`single-source`。

## 摘要(Summary)

阶段 G 在项目实际开发和部署期间提供架构监督。它确认部署范围和优先级，确保交付团队理解目标架构，使用架构合同明确项目范围、战略要求、符合性规则和路线图时间要求，并通过持续合规审查处理实现驱动的变更请求。

部署完成后，阶段 G 进行投产后审查，将已实现的业务和 IT 运行模型、系统及构建块发布为新的 [[baseline-architecture(基线架构)]]，更新架构存储库。阶段的重点是保持架构意图和实现之间的可追溯关系，而不是由架构团队取代项目开发。

![阶段G实施治理](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00125_img001.png)

## 目的和目标

- 确保实施项目符合 [[target-architecture(目标架构)]]。
- 对解决方案和实现引起的架构变更执行适当治理。

## 关键输入

最终架构定义、需求规格、路线图、实施迁移计划、治理框架、实施治理模型、架构合同和变更请求。

## 核心步骤

1. 与开发管理确认部署范围、优先级、差距和需替换的构建块。
2. 识别资源和技能，确保开发方法能够接收架构产物并反馈设计。
3. 为每个部署项目记录影响、战略需求、符合性规则、合同和时间约束。
4. 持续执行架构符合性审查和投产后审查。
5. 部署业务/IT 服务、培训和沟通成果，建立运行模型。
6. 发布新基线、更新存储库并关闭实施。

## 技术、关键决策和跨阶段依赖

- 技术：架构合同、架构符合性审查、实施审计、豁免管理、变更请求评估和投产后审查。
- 关键决策：部署范围和优先级如何落实、实现偏差是否可接受、何时批准豁免，以及何种变化必须回到架构治理。
- 跨阶段依赖：本阶段依据阶段 E/F 的路线图、计划和治理模型监督项目；已部署解决方案回写为新基线并交给阶段 H 持续监测。

## 主要输出

- 已签署的架构合同、合规评估、建议、豁免和变更请求。
- 符合架构的已部署解决方案及业务/IT 运行模型。
- 更新后的愿景、架构定义、性能度量、服务要求和存储库。
- 可复用 ABB。

## 关键主张(Key Claims)

1. 阶段 G 与组织的实际开发过程并行运行，架构治理不等于替代解决方案开发。[原文，§11.5，raw 页130](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 架构合同建立架构组织与实施组织之间的正式连接。[原文，§11.3.3、§11.5，raw 页128–131](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 采用过渡式部署可较早实现业务收益，并降低整体转型和迁移风险。[原文，§11.5，raw 页130–131](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 已部署解决方案必须回写为新基线，才能为后续运行、变更和新循环提供事实基础。[原文，§11.3.5–11.4，raw 页129–130](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[architecture-governance(架构治理)]]
- [[implementation-plan(实施计划)]]
- [[architecture-building-block(架构构建块)]]与[[solution-building-block(解决方案构建块)]]
- [[transition-architecture(过渡架构)]]
- [[baseline-architecture(基线架构)]]与[[target-architecture(目标架构)]]

## 重要引文(Notable Quotes)

> “Phase G establishes the connection between architecture and implementation organization.” — §11.5，raw 页131

## 局限／偏见(Limitations / Bias)

架构人员介入实现的深度由组织政策决定；本章提供治理边界，并不规定项目团队的具体开发流程。
