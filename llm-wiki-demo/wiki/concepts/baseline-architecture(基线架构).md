---
title: 基线架构
type: concept
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [architecture-state, baseline, as-is]
---

# 基线架构

> English: Baseline Architecture；状态：`single-source`。

## 定义

基线架构是对当前企业状态的架构描述，即进行目标决策时所使用的“现状”或 as-is 参照。它可以覆盖业务、数据、应用和技术域，并包含当前构建块、关系、标准、能力和约束。

## 在 ADM 中的作用

阶段 A 给出高层基线；阶段 B–D 只以支持目标决策和 [[gap-analysis(差距分析)]] 所需的详细程度完善各域基线。基线不必与 [[target-architecture(目标架构)]] 具有相同细节，已有架构材料应优先复用并验证。

阶段 G 将完成部署的解决方案及运行模型发布为新的基线，阶段 H 再持续监测其业务和技术变化。

## 边界

基线不是完整资产清单，也不是历史档案。只有影响当前目标、差距和迁移决策的现状才需要进入本轮基线描述。

## 相关页面

- [[target-architecture(目标架构)]]
- [[transition-architecture(过渡架构)]]
- [[gap-analysis(差距分析)]]
- [[architecture-scope(架构范围)]]
- [[architecture-repository(架构存储库)]]

## 证据

原文 §1.5.3、§3.3.6、阶段 B–D 的基线步骤及 §11.3.5 共同说明基线生命周期。[原始来源](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
