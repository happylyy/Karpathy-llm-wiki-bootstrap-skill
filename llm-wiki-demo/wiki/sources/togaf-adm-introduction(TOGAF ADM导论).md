---
title: TOGAF ADM导论
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, lifecycle, scope]
---

# TOGAF ADM导论

> 证据范围：第1章，raw 页16–30；状态：`single-source`。

## 摘要(Summary)

导论把 ADM 定义为开发和管理 [[target-architecture(目标架构)]] 生命周期的核心方法，并说明它如何借助 [[enterprise-continuum(企业连续统一体)]] 定位可复用资产、通过 [[architecture-repository(架构存储库)]] 保存这些资产。架构开发是持续循环：首次执行可复用材料较少，后续循环则不断积累企业特定的构建块和决策。

ADM 的使用边界并非由标准替组织决定。每轮都要在企业价值和资源约束下选择范围的广度、深度、时间跨度和架构域。原文也强调需要提出多个 [[architecture-alternative(架构替代方案)]]，再借助 [[trade-off-analysis(权衡分析)]]揭示隐藏需求并形成可接受的目标方案。

![架构替代方案方法](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00028_img001.png)

## 目的和目标

- 说明 [[architecture-development-cycle(架构开发周期)]] 的迭代结构及需求管理的中心地位。
- 决定本轮工作的广度、深度、时间、架构域和可复用资产。
- 让架构治理覆盖方法执行、产物状态、版本、批准和变更控制。
- 对候选目标架构建立准则，比较、选择或组合替代方案。
- 对分区或联邦式架构建立一致的参考框架，管理集成、复用和符合性关系。

## 关键输入

组织的业务需求和价值目标、利益相关者关注点、既有架构资产与存储库、治理和项目管理约束、可用资源，以及对架构范围和时间跨度的初步判断。

## 核心步骤

1. 理解 ADM 在循环、阶段之间和阶段内部的迭代方式。
2. 确定架构范围、架构域、详细程度、时间跨度和分区关系。
3. 盘点可复用的参考资产、企业资产和构建块。
4. 建立产物状态、版本、批准、符合性和变更控制规则。
5. 构造候选架构并通过明确准则执行权衡和整合。

## 技术、关键决策和跨阶段依赖

- 技术：企业连续统一体分类、架构存储库复用、架构分区、替代方案构造和权衡分析。
- 关键决策：本轮 ADM 覆盖什么、做到多深、采用哪些域、复用哪些资产，以及如何处理候选方案冲突。
- 跨阶段依赖：本章为预备阶段和阶段 A–H 设定共同执行规则；需求管理持续把各阶段的新需求和变化送回相关位置。

## 关键主张(Key Claims)

1. ADM 是 TOGAF 标准的核心，并把标准中的架构资产整合为满足组织业务需要的开发方法。[原文，§1.1，raw 页16](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 企业连续统一体负责分类和提供上下文，架构存储库则是保存、治理和复用资产的实际实现，两者不能合并为一个概念。[原文，§1.1.1，raw 页16–17](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 范围必须同时考虑广度、深度、时间和架构域；范围过宽或过深都可能削弱利益相关者价值。[原文，§1.5，raw 页23–27](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 单一方案通常不能满足所有关注点，架构师应显式呈现替代方案和权衡，再选择或组合目标方案。[原文，§1.6，raw 页27–28](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
5. 架构整合受制于产物粒度、详细程度和交换标准成熟度，需要持续的标准治理和冲突处理。[原文，§1.7，raw 页28–29](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 主要输出

导论本身不规定单独的正式交付物，但为后续阶段建立以下决策基础：本轮范围、迭代方式、资产复用策略、治理要求、产物状态规则、架构域组合以及替代方案选择方法。

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[architecture-development-cycle(架构开发周期)]]
- [[enterprise-continuum(企业连续统一体)]]与[[architecture-repository(架构存储库)]]
- [[architecture-scope(架构范围)]]
- [[architecture-governance(架构治理)]]
- [[architecture-alternative(架构替代方案)]]与[[trade-off-analysis(权衡分析)]]
- [[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]]、[[transition-architecture(过渡架构)]]

## 重要引文(Notable Quotes)

> “The depth and detail ... needs to be sufficient for its purpose, and no more.” — §1.5.2，raw 页25

## 局限／偏见(Limitations / Bias)

导论说明 tailoring 是必要的执行活动，但按本 Wiki 的持久化边界不把它建立为独立概念页；具体调整仍需在预备阶段和阶段 A 的来源页中保留。
