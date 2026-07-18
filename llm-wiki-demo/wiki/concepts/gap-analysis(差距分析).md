---
title: 差距分析
type: concept
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [architecture, gap-analysis, roadmap]
---

# 差距分析

> English: Gap Analysis；状态：`single-source`。

## 定义

差距分析是比较 [[baseline-architecture(基线架构)]] 与 [[target-architecture(目标架构)]]，识别必须新增、保留、改变或消除的能力、构建块和关系的过程。

## 在 ADM 中的作用

阶段 B–D 在验证模型一致性、原则和需求完整性后执行各域差距分析，并把结果转为候选路线图组件。阶段 E 将四域差距与解决方案、实施因素和依赖整合，识别 SBB 和 [[work-package(工作包)]]。需求管理还会重新检查过去阶段的差距。

原文区分两类表面差距：基线有而目标无，以及基线无而目标有。前者可能是有意淘汰，也可能是意外遗漏；意外遗漏会产生需要修正目标架构的“差距需求”。

## 边界

差距不是脱离语境的差异清单。只有相对于当前业务需求、范围、价值和目标有意义的差异，才应进入路线图和需求管理。

## 相关页面

- [[baseline-architecture(基线架构)]]
- [[target-architecture(目标架构)]]
- [[architecture-roadmap(架构路线图)]]
- [[solution-building-block(解决方案构建块)]]
- [[architecture-requirements-management(架构需求管理)]]

## 证据

阶段 B–D 定义各域差距，§9.3.3 汇总差距，§13.3 解释差距需求。[原始来源](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
