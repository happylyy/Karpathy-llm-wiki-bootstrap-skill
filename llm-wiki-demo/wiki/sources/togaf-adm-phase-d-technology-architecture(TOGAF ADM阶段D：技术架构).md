---
title: TOGAF ADM阶段D：技术架构
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, phase-d, technology-architecture]
---

# TOGAF ADM阶段D：技术架构

> 证据范围：第8章，raw 页94–106；状态：`single-source`。

## 摘要(Summary)

阶段 D 定义支撑愿景及目标业务、数据、应用构建块的 [[technology-architecture(技术架构)]]。它建立技术服务和逻辑组件分类，盘点部署位置和物理产品，把现状抽象到统一分类中，再依据应用和业务需求判断现有技术是否适用并完成目标配置。

技术架构需要处理性能、可维护性、位置与延迟、可用性、容量、成本、标准符合性及迁移影响。新兴技术不仅被动接收上层需求，也可能成为新的业务能力和架构变更驱动因素。

![阶段D技术架构](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00094_img001.png)

## 目的和目标

- 定义能够实现目标业务、数据和应用构建块的目标技术架构。
- 从技术基线和目标之间的差距中提出候选路线图组件。

## 关键输入

技术原则、产品信息、架构愿景、业务/数据/应用差距与需求、架构存储库、组织标准及已有路线图组件。

## 核心步骤

1. 选择技术参考模型、视点和工具，建立服务及组件分类。
2. 盘点部署技术、位置、平台栈、环境、网络和容量，并映射到统一分类。
3. 依据功能和非功能需求选择服务、产品及配置。
4. 建立必要的基线和目标技术描述，执行差距及替代方案分析。
5. 评估成本、容量、安装、治理、迁移和跨项目影响。
6. 完成技术构建块、接口、需求可追溯性和路线图组件。

## 技术、关键决策和跨阶段依赖

- 技术：技术组合盘点、服务和标准分类、环境及位置图、平台分解、容量和质量属性分析、新兴技术评估及差距分析。
- 关键决策：逻辑服务如何映射物理组件、采用哪些标准和产品约束、怎样满足非功能需求，以及哪些技术变化进入路线图。
- 跨阶段依赖：本阶段实现业务、数据和应用架构提出的要求；技术限制或机会可以反馈先前阶段，其差距和构建块进入阶段 E。

## 主要输出

- 获批的基线和目标技术架构。
- 技术服务、平台栈、环境、位置、网络、硬件和处理负载视图。
- 技术需求、标准、接口和四域差距的技术响应。
- 技术架构路线图组件。

## 关键主张(Key Claims)

1. 技术架构必须把产品盘点抽象为稳定的服务和组件分类，才能比较基线和目标。[原文，§8.3.1.1–8.3.2，raw 页97–101](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 服务粒度会影响性能、维护、延迟和可用性，服务边界不能脱离平台及位置约束讨论。[原文，§8.3.1.1，raw 页98](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. [[architecture-building-block(架构构建块)]]描述功能及可能实现方式，但不引入配置和详细设计。[原文，§8.3.3，raw 页101–102](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 新兴技术既可响应信息系统需求，也可主动驱动业务能力和战略变化。[原文，§8.5.1，raw 页104–105](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[technology-architecture(技术架构)]]
- [[business-architecture(业务架构)]]、[[data-architecture(数据架构)]]、[[application-architecture(应用架构)]]
- [[architecture-building-block(架构构建块)]]
- [[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]]与[[gap-analysis(差距分析)]]
- [[architecture-roadmap(架构路线图)]]

## 重要引文(Notable Quotes)

> “The Technology Architecture may both drive business capabilities and respond to information system requirements.” — §8.5.1，raw 页105

## 局限／偏见(Limitations / Bias)

标准提供技术分类和决策框架，不推荐具体产品；产品选择仍需依据时间敏感的市场、成本、安全和组织约束。
