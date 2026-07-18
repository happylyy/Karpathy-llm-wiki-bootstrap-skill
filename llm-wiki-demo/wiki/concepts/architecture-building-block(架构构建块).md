---
title: 架构构建块
type: concept
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [building-block, architecture, abb]
---

# 架构构建块

> English: Architecture Building Block (ABB)；状态：`single-source`。

## 定义

架构构建块描述架构所需的能力或功能，以及可能的实现方式，但不引入具体产品配置或详细解决方案设计。它是业务、数据、应用或技术目标架构中可复用、可组合和可治理的规格单元。

## 在 ADM 中的作用

阶段 A 可从存储库复用 ABB 形成高层愿景；阶段 B–D 识别、定义、验证并发布各域 ABB；阶段 E 根据 ABB 和差距确定实现它们的 [[solution-building-block(解决方案构建块)]]；阶段 F 将可复用 ABB 纳入最终输出；阶段 G 检查实现是否符合其要求。

ABB 为目标架构和解决方案之间提供稳定边界：前者说明“必须具备什么”，后者说明“由什么具体机制实现”。

## 边界

ABB 不是产品、项目或部署单元。一个 ABB 可由多个 SBB 实现，一个 SBB 也可能支持多个 ABB。

## 相关页面

- [[solution-building-block(解决方案构建块)]]
- [[architecture-repository(架构存储库)]]
- [[target-architecture(目标架构)]]
- [[gap-analysis(差距分析)]]
- [[work-package(工作包)]]

## 证据

原文 §8.3.3、§9.1、§9.3.3、§10.4 和 §11.4 说明 ABB 从设计到实现治理的角色。[原始来源](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
