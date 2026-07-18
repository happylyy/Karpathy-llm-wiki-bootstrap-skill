---
title: 迁移计划
type: concept
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [migration, planning, transition]
---

# 迁移计划

> English: Migration Plan；状态：`single-source`。这是对官方复合产物 “Implementation and Migration Plan” 的分析性拆分。

## 定义

迁移计划描述企业如何从 [[baseline-architecture(基线架构)]] 经过必要的 [[transition-architecture(过渡架构)]] 到达 [[target-architecture(目标架构)]]，重点处理顺序、依赖、切换策略、数据/系统迁移、风险和企业吸收变化的节奏。

## 在 ADM 中的作用

阶段 E 依据差距依赖、准备度、风险及绿地、革命式或演进式策略形成迁移方向。阶段 F 通过业务价值、成本收益、风险和资源可用性确认迁移项目顺序，把过渡架构作为投资组合里程碑并完成正式计划。

迁移计划受到现有 SBB 生命周期、外部依赖和能力增量约束；单纯按技术便利排序不能保证业务价值。

## 边界

本概念强调状态转换和次序，区别于 [[implementation-plan(实施计划)]] 对项目、活动、资源和治理的组织。两者在官方交付物中仍保持一体。

## 相关页面

- [[implementation-plan(实施计划)]]
- [[transition-architecture(过渡架构)]]
- [[architecture-roadmap(架构路线图)]]
- [[work-package(工作包)]]
- [[business-value(业务价值)]]

## 证据

原文 §9.3.6–9.3.11 和第10章说明依赖、迁移策略、排序及计划完成过程。[原始来源](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
