---
title: 数据架构
type: concept
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [architecture-domain, data-architecture]
---

# 数据架构

> English: Data Architecture；状态：`single-source`。

## 定义

数据架构描述企业数据的概念、逻辑和物理结构，以及数据如何被创建、保存、流动、使用、交换、迁移、保护、治理和归档。它覆盖静态数据、流动数据、使用中数据和开放数据。

## 在 ADM 中的作用

阶段 C 根据业务信息和能力需求建立基线及目标数据架构。架构师统一数据目录和语义，把数据映射到业务服务、能力、职能、访问权和应用，并通过 [[gap-analysis(差距分析)]] 识别缺失、重复或无人负责的数据。

数据架构向 [[application-architecture(应用架构)]] 和 [[technology-architecture(技术架构)]] 提供互操作、迁移、质量、安全及管理要求，也可能根据应用发现触发短迭代。

## 边界

数据架构不是某个数据库模式。架构级描述需要连接业务语义和跨系统关系；详细物理模式只有在当前决策需要时才纳入。

## 相关页面

- [[togaf-adm-phase-c-data-architecture(TOGAF ADM阶段C：数据架构)]]
- [[business-architecture(业务架构)]]
- [[application-architecture(应用架构)]]
- [[architecture-building-block(架构构建块)]]
- [[architecture-roadmap(架构路线图)]]

## 证据

原文第6章说明数据架构的建模、差距、数据管理、迁移和治理要求。[原始来源](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
