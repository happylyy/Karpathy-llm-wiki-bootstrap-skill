---
title: 解决方案构建块
type: concept
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [building-block, solution, sbb]
---

# 解决方案构建块

> English: Solution Building Block (SBB)；状态：`single-source`。

## 定义

解决方案构建块是实现一个或多个 [[architecture-building-block(架构构建块)]] 的具体解决方案级构件。它可以是新开发、既有系统增强、可采购产品、第三方服务或这些机制的组合。

## 在 ADM 中的作用

阶段 E 根据综合差距、候选路线图组件和 ABB 识别 SBB，并在解决方案及依赖矩阵中说明每个差距由何种机制解决。SBB 的互操作冲突要通过转换构建块或修改冲突规格处理。

阶段 F 将 SBB 的成本、收益、资源、风险和依赖纳入项目排序；阶段 G 由解决方案架构师细化 SBB 与项目的映射，并通过符合性审查保证实现不偏离目标架构。

## 边界

SBB 比 ABB 更具体，但仍可以跨项目复用。它不等同于工作包：SBB 是解决方案构件，[[work-package(工作包)]] 是需要协同交付的一组变更活动。

## 相关页面

- [[architecture-building-block(架构构建块)]]
- [[gap-analysis(差距分析)]]
- [[work-package(工作包)]]
- [[implementation-plan(实施计划)]]
- [[architecture-governance(架构治理)]]

## 证据

原文 §9.1、§9.3.3、§9.3.9、§10.3.4 和 §11.3.1 说明 SBB 的识别及治理。[原始来源](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
