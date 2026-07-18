---
title: TOGAF ADM架构需求管理
type: source-summary
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [togaf, adm, requirements-management]
---

# TOGAF ADM架构需求管理

> 证据范围：第13章，raw 页142–150；状态：`single-source`。

## 摘要(Summary)

[[architecture-requirements-management(架构需求管理)]] 位于 ADM 循环中心，是贯穿所有阶段和多个循环的动态过程。它识别、记录、监测和传递需求及其变化，保证每个阶段能够取得已批准需求，并把阶段中产生的新需求送入正确的后续工作或需求存储库。

需求管理本身不解决或排序需求；责任仍属于受到影响的 ADM 阶段及相关利益相关者。需求发生变化时，需要生成需求影响评估，确定对当前阶段、已完成阶段、时间、成本和业务度量的影响，再决定立即实现、返回先前阶段还是推迟到后续循环。

![ADM架构需求管理](../../raw/C220-Part1e-Architecture%20Development%20Method_images/p00142_img001.png)

## 目的和目标

- 维持覆盖全部相关阶段的需求管理过程。
- 管理任意阶段或循环中识别的架构需求。
- 保证每个阶段都能取得相关、已批准且状态最新的需求。

## 关键输入

架构存储库、组织模型、工作说明、架构愿景、架构需求规格、需求影响评估，以及各阶段产生或修改的需求。

## 核心步骤

1. 识别需求并写入需求规格和需求存储库。
2. 建立基线需求、优先级和利益相关者共识。
3. 持续监测基线，识别新增、修改或应删除的需求。
4. 记录变化、冲突和优先级并生成需求影响评估。
5. 分析变化对当前及过去阶段的影响，决定立即实施或延期。
6. 更新需求存储库和当前阶段产物，并重新检查阶段 B–D 的差距分析。

## 技术、关键决策和跨阶段依赖

- 技术：需求存储库、需求基线、状态跟踪、可追溯性、需求影响评估、冲突记录及差距复核。
- 关键决策：新需求是否属于当前范围、变化立即处理还是延期、哪些阶段受影响，以及应返回哪个阶段作出实质决策。
- 跨阶段依赖：每个 ADM 阶段既消费已批准需求，也产生或修改需求；本过程在阶段之间传递变化，并把阶段 H 的请求送入当前或下一循环。

## 主要输出

- 需求影响评估。
- 更新后的架构需求规格。
- 跨循环保存全部需求信息的架构需求存储库。

## 关键主张(Key Claims)

1. ADM 中心的需求管理代表动态过程，而不是一组静态需求。[原文，§13.5.1，raw 页147–148](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
2. 需求管理负责流转和状态，具体处置及优先级仍由相关阶段决定。[原文，§13.5.1，raw 页147](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
3. 需求规格描述当前循环的正式需求，需求影响评估描述变化影响，需求存储库则可跨多个循环保存完整历史。[原文，§13.4–13.5.1，raw 页146–148](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
4. 阶段内新产生且超出当前工作说明范围的需求，应进入需求存储库而非扩大当前项目范围。[原文，§13.5.2，raw 页148](../../raw/C220-Part1e-Architecture%20Development%20Method.md)
5. 差距分析发现“意外消除”的内容时，会产生需要修改目标架构的差距需求。[原文，§13.3，raw 页146](../../raw/C220-Part1e-Architecture%20Development%20Method.md)

## 提及的实体(Entities Mentioned)

- [[the-open-group(开放群组)]]
- [[togaf-standard(TOGAF标准)]]

## 相关概念(Concepts)

- [[architecture-requirements-management(架构需求管理)]]
- [[architecture-development-cycle(架构开发周期)]]
- [[stakeholder-concern(利益相关者关注点)]]
- [[gap-analysis(差距分析)]]
- [[architecture-vision(架构愿景)]]
- [[value-stream(价值流)]]

## 重要引文(Notable Quotes)

> “The Requirements Management process itself does not dispose of, address, or prioritize any requirements.” — §13.5.1，raw 页147

## 局限／偏见(Limitations / Bias)

TOGAF 只规定有效需求管理应达到什么结果，不强制具体需求工程流程或工具；实现仍需结合组织方法。
