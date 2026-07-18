---
title: TOGAF架构开发方法
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, enterprise-architecture, method]
---

# TOGAF架构开发方法

> 状态：`single-source`。本页是《TOGAF Standard — Architecture Development Method》的中文方法入口，同时代表本 Wiki 中的 ADM 方法页。

## 摘要(Summary)

架构开发方法（Architecture Development Method, ADM）是 [[togaf-standard(TOGAF标准)]] 的核心。它把企业架构工作组织成一个持续迭代的生命周期：先建立架构能力和治理基础，再形成愿景，依次开发业务、数据、应用和技术架构，随后把差距转换为可交付的工作包、过渡状态和迁移安排，并通过实施治理和变更管理维持架构的有效性。

ADM 不是固定的瀑布流程。每次循环都要根据业务价值、利益相关者关注点、可用资源和组织成熟度重新确定范围、详细程度、时间跨度、架构域及可复用资产。[[architecture-requirements-management(架构需求管理)]] 位于循环中心，持续把新增或变化的需求送入相关阶段。

来源由 [[the-open-group(开放群组)]] 发布，原版于 2022 年 4 月发布，2025 年 5 月纳入 Technical Corrigendum 1。本文档是规范性方法说明，不等同于完整 TOGAF 文档集；内容框架、详细技术和能力治理等主题由其他 TOGAF 文档补充。

## 文档信息

| Field(字段) | Value(值) |
| --- | --- |
| 原始标题 | TOGAF® Standard — Architecture Development Method |
| 文档编号 | C220 |
| 发布者 | [[the-open-group(开放群组)]] |
| 版本信息 | 2022-04 发布；2025-05 更新 |
| 主要受众 | 企业、业务、数据、应用、系统、解决方案及 IT 架构师 |
| 本地证据 | [原始 Markdown](../../raw/C220-Part1e-Architecture%20Development%20Method.md) |

![ADM架构开发周期](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00019_img001.png)

## 关键主张(Key Claims)

1. ADM 是开发并管理企业架构生命周期的方法，也是 TOGAF 标准的核心。[原文，§1.1，raw 页16–17](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. ADM 在整个过程、阶段之间和阶段内部都具有迭代性；每轮都需要重新作出范围和资产复用决策。[原文，§1.2，raw 页18–20](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 业务、数据、应用和技术架构域共享“[[baseline-architecture(基线架构)]]—[[target-architecture(目标架构)]]—[[gap-analysis(差距分析)]]—路线图组件”的开发模式。[原文，第4–8章，raw 页56–106](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 架构交付不是文档终点：阶段 E/F 将差距转化为 [[work-package(工作包)]]、[[transition-architecture(过渡架构)]]、[[architecture-roadmap(架构路线图)]]和实施迁移安排。[原文，第9–10章，raw 页106–125](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
5. 实施治理、价值实现、变更管理和动态需求管理共同关闭反馈循环，使架构随企业持续演化。[原文，第11–13章，raw 页125–150](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 阶段导航

1. [[togaf-adm-introduction(TOGAF ADM导论)]]：循环结构、适用范围、资产复用、治理和替代方案。
2. [[togaf-adm-preliminary-phase(TOGAF ADM预备阶段)]]：建立企业架构能力、组织、原则和治理框架。
3. [[togaf-adm-phase-a-architecture-vision(TOGAF ADM阶段A：架构愿景)]]：明确价值、范围和利益相关者承诺。
4. [[togaf-adm-phase-b-business-architecture(TOGAF ADM阶段B：业务架构)]]：定义目标业务运作方式。
5. [[togaf-adm-phase-c-information-systems-architectures(TOGAF ADM阶段C：信息系统架构)]]：协调数据和应用架构。
6. [[togaf-adm-phase-c-data-architecture(TOGAF ADM阶段C：数据架构)]]：定义数据结构、流动、管理和治理。
7. [[togaf-adm-phase-c-application-architecture(TOGAF ADM阶段C：应用架构)]]：定义应用组合、服务和组件。
8. [[togaf-adm-phase-d-technology-architecture(TOGAF ADM阶段D：技术架构)]]：定义实现上层架构的技术平台和服务。
9. [[togaf-adm-phase-e-opportunities-and-solutions(TOGAF ADM阶段E：机会与解决方案)]]：把跨域差距组织成可交付变更。
10. [[togaf-adm-phase-f-migration-planning(TOGAF ADM阶段F：迁移规划)]]：按价值、成本和风险完成迁移排序。
11. [[togaf-adm-phase-g-implementation-governance(TOGAF ADM阶段G：实施治理)]]：监督项目对目标架构的符合性。
12. [[togaf-adm-phase-h-architecture-change-management(TOGAF ADM阶段H：架构变更管理)]]：监测价值和变化并决定维护或启动新循环。
13. [[togaf-adm-architecture-requirements-management(TOGAF ADM架构需求管理)]]：持续管理全部阶段的动态需求。

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 核心概念集群

- 方法基础：[[architecture-development-cycle(架构开发周期)]]、[[architecture-scope(架构范围)]]、[[enterprise-architecture-capability(企业架构能力)]]、[[architecture-principles(架构原则)]]、[[architecture-governance(架构治理)]]。
- 知识复用：[[enterprise-continuum(企业连续统一体)]]、[[architecture-repository(架构存储库)]]。
- 架构描述：[[architecture-vision(架构愿景)]]、[[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]]、[[transition-architecture(过渡架构)]]。
- 架构域：[[business-architecture(业务架构)]]、[[data-architecture(数据架构)]]、[[application-architecture(应用架构)]]、[[technology-architecture(技术架构)]]。
- 交付闭环：[[architecture-roadmap(架构路线图)]]、[[work-package(工作包)]]、[[implementation-plan(实施计划)]]、[[migration-plan(迁移计划)]]、[[value-realization(价值实现)]]。

## 重要引文(Notable Quotes)

> “The ADM is iterative, over the whole process, between phases, and within phases.” — §1.2.1，raw 页18

> “The key is to focus on the final target while realizing incremental business value.” — §9.5，raw 页115

## 局限／偏见(Limitations / Bias)

- 本 Wiki 当前只摄取这一份官方规范，全部判断均为 `single-source`，尚无案例研究或其他框架用于交叉验证。
- 原文描述的是通用方法，实际阶段顺序、产物、详细程度和治理机制必须结合组织环境决定。
- 原文版权页明确限制复制和将出版物用于生成式 AI。本 Wiki 仅为用户提供材料的私有研究性摘要，保留短引文和定位信息，不替代或再发布原标准。
