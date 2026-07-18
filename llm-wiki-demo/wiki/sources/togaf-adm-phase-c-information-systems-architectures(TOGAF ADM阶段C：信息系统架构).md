---
title: TOGAF ADM阶段C：信息系统架构
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-c, information-systems]
---

# TOGAF ADM阶段C：信息系统架构

> 证据范围：第5章，raw 页71–73；状态：`single-source`。

## 摘要(Summary)

阶段 C 是 [[data-architecture(数据架构)]] 和 [[application-architecture(应用架构)]] 的组合入口。其目标是让信息系统架构支持目标业务架构和架构愿景，并根据数据与应用的基线—目标差距形成候选路线图组件。

标准不强制两者的固定先后顺序。数据驱动方法先澄清核心数据和关系；应用驱动方法则可能围绕 ERP、CRM 等关键应用及其集成展开。二者在执行中可以短周期往返，以解决模型之间的依赖和约束。

![阶段C信息系统架构](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00071_img001.png)

## 目的和目标

- 开发支持业务架构及愿景的目标信息系统架构。
- 从数据和应用架构的差距中产生候选路线图组件。
- 根据企业环境选择“数据先行”“应用先行”或迭代组合。
- 具体步骤分别由 [[togaf-adm-phase-c-data-architecture(TOGAF ADM阶段C：数据架构)]] 和 [[togaf-adm-phase-c-application-architecture(TOGAF ADM阶段C：应用架构)]] 定义。

## 关键输入

获批的架构愿景、目标业务架构、业务差距和路线图组件、数据及应用原则、架构需求、既有信息系统资产、参考模型、标准和可复用构建块。

## 核心步骤

1. 根据核心资产和问题选择数据先行、应用先行或短周期迭代。
2. 执行数据架构子阶段，形成数据基线、目标、差距和约束。
3. 执行应用架构子阶段，形成应用基线、目标、差距和约束。
4. 在数据责任、应用集成和模型冲突处往返校正。
5. 合并两个子阶段的需求、影响和候选路线图组件。

## 技术、关键决策和跨阶段依赖

- 技术：数据及应用参考模型、目录、矩阵、关系图、组合分析和集成依赖分析。
- 关键决策：两个子阶段的先后顺序、往返次数、模型粒度，以及数据和应用边界如何协调。
- 跨阶段依赖：阶段 C 接收阶段 B 的业务语境；其结果为阶段 D 提供平台和部署约束，并在阶段 E 汇入跨域路线图。

## 关键主张(Key Claims)

1. 数据和应用是信息系统架构的两个互补部分，必须共同支撑业务架构。[原文，§5.1，raw 页72](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 阶段 C 不规定唯一顺序；顺序应由组织的核心资产、问题和集成挑战决定。[原文，§5.2，raw 页72–73](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 关键应用可能同时带有技术基础设施和业务逻辑，因此应用驱动方法仍需处理数据及技术依赖。[原文，§5.2，raw 页72–73](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 无论采用何种顺序，最终都要把数据与应用差距汇入跨域路线图。[原文，§5.1–5.2，raw 页72–73](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 主要输出

本章本身是阶段入口；正式输出由数据和应用两个子阶段共同构成，包括基线/目标架构、需求、差距结果和路线图组件。

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[data-architecture(数据架构)]]
- [[application-architecture(应用架构)]]
- [[business-architecture(业务架构)]]
- [[architecture-roadmap(架构路线图)]]

## 重要引文(Notable Quotes)

> “Phase C involves some combination of Data and Application Architecture, in either order.” — §5.2，raw 页72

## 局限／偏见(Limitations / Bias)

第5章只给出组合逻辑，不应脱离第6章和第7章单独作为完整执行指南。
