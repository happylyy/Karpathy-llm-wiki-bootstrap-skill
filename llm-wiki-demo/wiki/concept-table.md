---
title: Concept Table
type: concept-table
created: 2026-07-18
updated: 2026-07-18
sources: [C220-Part1e-Architecture Development Method.md]
tags: [concept-map, navigation, maintenance, togaf, adm]
---

> 此表是 Wiki 的压缩概念地图。索引用于编目页面；此表用于说明 32 个持久概念的含义、相互关系及维护边界。

## 维护规则

- 为 wiki/concepts/ 下的每个持久概念页面保留一行。
- 每当创建、重命名、删除、合并、拆分或实质性修订概念页面时，更新此表。
- 按概念页面的英文 slug 字母顺序排列各行。
- 定义应简洁并体现证据情况；详细内容链接到完整概念页面。
- 当前全部概念只由一个官方来源支持，因此状态统一为 single-source。
- 复合术语在证据允许时拆分为独立概念；持久概念标题不使用“与”连接两个概念。

## 概念

| Concept(概念) | Working definition(工作定义) | Role in this wiki(作用) | Sources(来源) | Related pages(相关页面) | Status(状态) | Maintenance note(维护备注) |
| --- | --- | --- | --- | --- | --- | --- |
| [[application-architecture(应用架构)]] | 支持业务和数据需要的应用服务、组件、功能分布及其关系。 | 阶段 C 形成应用基线、目标、差距和路线图组件。 | C220-Part1e-Architecture Development Method.md | [[data-architecture(数据架构)]]、[[technology-architecture(技术架构)]] | single-source | 与详细软件设计保持边界。 |
| [[architecture-alternative(架构替代方案)]] | 满足愿景、原则和需求的候选目标架构或候选路径。 | 为阶段 B–E 的显式选择提供待评估对象。 | C220-Part1e-Architecture Development Method.md | [[trade-off-analysis(权衡分析)]]、[[target-architecture(目标架构)]] | single-source | 不与决策方法或最终决策合并。 |
| [[architecture-building-block(架构构建块)]] | 描述所需能力或功能但不锁定具体产品的架构规格单元。 | 连接目标架构需求和解决方案实现。 | C220-Part1e-Architecture Development Method.md | [[solution-building-block(解决方案构建块)]]、[[target-architecture(目标架构)]] | single-source | 保持 ABB 和 SBB 的双向区分。 |
| [[architecture-change-management(架构变更管理)]] | 持续监测架构和环境并决定维护、局部重构或新 ADM 循环的治理过程。 | 阶段 H 关闭实施反馈并启动后续演进。 | C220-Part1e-Architecture Development Method.md | [[value-realization(价值实现)]]、[[architecture-development-cycle(架构开发周期)]] | single-source | 不等同于项目或服务变更控制。 |
| [[architecture-development-cycle(架构开发周期)]] | 从能力准备到持续变更的迭代 ADM 生命周期。 | 组织预备阶段、A–H 阶段和贯穿式需求管理。 | C220-Part1e-Architecture Development Method.md | [[architecture-requirements-management(架构需求管理)]]、[[architecture-change-management(架构变更管理)]] | single-source | 避免解释为固定顺序的一次性流程。 |
| [[architecture-governance(架构治理)]] | 管理架构决策、产物、实施、合规和变更的责任及控制体系。 | 贯穿能力建立、阶段批准、实施监督和变更裁决。 | C220-Part1e-Architecture Development Method.md | [[enterprise-architecture-capability(企业架构能力)]]、[[architecture-repository(架构存储库)]] | single-source | 与设计活动及项目管理分开。 |
| [[architecture-principles(架构原则)]] | 约束架构开发、选择和实施的一组稳定规则。 | 为范围、模型、替代方案和标准选择提供共同准则。 | C220-Part1e-Architecture Development Method.md | [[architecture-governance(架构治理)]]、[[trade-off-analysis(权衡分析)]] | single-source | 不与详细需求或技术标准混淆。 |
| [[architecture-repository(架构存储库)]] | 保存并治理架构资产、版本、状态和审计信息的受控环境。 | 支持跨 ADM 循环的复用、发布和更新。 | C220-Part1e-Architecture Development Method.md | [[enterprise-continuum(企业连续统一体)]]、[[architecture-governance(架构治理)]] | single-source | 与分类框架企业连续统一体分开。 |
| [[architecture-requirements-management(架构需求管理)]] | 跨阶段和循环识别、记录、传递、监测及追踪架构需求的动态过程。 | 贯穿 ADM 并管理阶段间需求反馈。 | C220-Part1e-Architecture Development Method.md | [[architecture-development-cycle(架构开发周期)]]、[[gap-analysis(差距分析)]] | single-source | 不替代需求的解决和优先级决策。 |
| [[architecture-roadmap(架构路线图)]] | 从基线到目标的时间化演进描述。 | 排列工作包、能力增量和过渡架构。 | C220-Part1e-Architecture Development Method.md | [[work-package(工作包)]]、[[transition-architecture(过渡架构)]] | single-source | 与详细项目进度表保持边界。 |
| [[architecture-scope(架构范围)]] | 对架构工作的广度、深度、时间跨度和架构域边界的约定。 | 控制阶段 A 及后续工作的投入和详细程度。 | C220-Part1e-Architecture Development Method.md | [[stakeholder-concern(利益相关者关注点)]]、[[business-value(业务价值)]] | single-source | 明确范围内外，不追求无条件完整。 |
| [[architecture-viewpoint(架构视点)]] | 构造、选择和解释架构视图以回应特定关注点的约定。 | 把利益相关者问题映射到模型、目录、矩阵和图。 | C220-Part1e-Architecture Development Method.md | [[stakeholder-concern(利益相关者关注点)]]、[[architecture-vision(架构愿景)]] | single-source | 与具体视图及关注点分开。 |
| [[architecture-vision(架构愿景)]] | 对拟议目标架构及其价值、范围和约束的高层一致理解。 | 阶段 A 获取授权并为 B–D 阶段定向。 | C220-Part1e-Architecture Development Method.md | [[target-architecture(目标架构)]]、[[business-value(业务价值)]] | single-source | 保持高层决策粒度。 |
| [[baseline-architecture(基线架构)]] | 范围内当前架构状态的必要描述。 | 为各域差距分析和迁移判断提供起点。 | C220-Part1e-Architecture Development Method.md | [[target-architecture(目标架构)]]、[[transition-architecture(过渡架构)]] | single-source | 只保留影响目标判断的现状细节。 |
| [[business-architecture(业务架构)]] | 描述业务战略、治理、组织、能力、价值流和流程的架构域。 | 阶段 B 为数据、应用和技术架构提供业务语境。 | C220-Part1e-Architecture Development Method.md | [[business-capability(业务能力)]]、[[value-stream(价值流)]] | single-source | 与单一流程设计或组织设计分开。 |
| [[business-capability(业务能力)]] | 企业为实现目标所需的稳定能力表达。 | 连接战略、价值流、组织和路线图优先级。 | C220-Part1e-Architecture Development Method.md | [[value-stream(价值流)]]、[[business-architecture(业务架构)]] | single-source | 不把能力等同于组织单元或流程。 |
| [[business-value(业务价值)]] | 架构选择或工作包预计产生的业务收益及优先级依据。 | 支持愿景、方案评估、工作包排序和路线图决策。 | C220-Part1e-Architecture Development Method.md | [[value-realization(价值实现)]]、[[work-package(工作包)]] | single-source | 与部署后的价值验证分开。 |
| [[data-architecture(数据架构)]] | 描述企业数据实体、逻辑和物理组件、治理及流动关系的架构域。 | 阶段 C 形成数据基线、目标、差距和路线图组件。 | C220-Part1e-Architecture Development Method.md | [[application-architecture(应用架构)]]、[[business-architecture(业务架构)]] | single-source | 与数据库物理设计保持边界。 |
| [[enterprise-architecture-capability(企业架构能力)]] | 组织持续开展、治理和改进企业架构工作的能力。 | 预备阶段建立组织、流程、角色、工具和成熟度基础。 | C220-Part1e-Architecture Development Method.md | [[architecture-governance(架构治理)]]、[[architecture-repository(架构存储库)]] | single-source | 不把能力缩减为单次项目团队。 |
| [[enterprise-continuum(企业连续统一体)]] | 从通用到企业特定组织和理解架构及解决方案资产的分类框架。 | 帮助发现、定位和复用存储库资产。 | C220-Part1e-Architecture Development Method.md | [[architecture-repository(架构存储库)]]、[[architecture-building-block(架构构建块)]] | single-source | 与实际资产存储环境分开。 |
| [[gap-analysis(差距分析)]] | 比较基线和目标并识别新增、保留、改变或消除项的过程。 | 阶段 B–E 将架构差异转化为需求和路线图组件。 | C220-Part1e-Architecture Development Method.md | [[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]] | single-source | 只持久化有业务和架构意义的差异。 |
| [[implementation-plan(实施计划)]] | 组织路线图所需项目、活动、资源、成本、里程碑和治理的计划视角。 | 阶段 E/F 形成，阶段 G 用于实施启动和监督。 | C220-Part1e-Architecture Development Method.md | [[migration-plan(迁移计划)]]、[[architecture-roadmap(架构路线图)]] | single-source | 官方复合产物保留原名，本页仅作分析性拆分。 |
| [[migration-plan(迁移计划)]] | 规定从基线经中间状态到目标的顺序、依赖、切换和风险的计划视角。 | 阶段 E/F 确认迁移策略和项目次序。 | C220-Part1e-Architecture Development Method.md | [[implementation-plan(实施计划)]]、[[transition-architecture(过渡架构)]] | single-source | 官方复合产物保留原名，本页仅作分析性拆分。 |
| [[solution-building-block(解决方案构建块)]] | 实现一个或多个架构构建块的具体解决方案级构件。 | 阶段 E 连接差距、解决机制和项目交付。 | C220-Part1e-Architecture Development Method.md | [[architecture-building-block(架构构建块)]]、[[work-package(工作包)]] | single-source | 与工作包及具体项目分开。 |
| [[stakeholder-concern(利益相关者关注点)]] | 利益相关者关心的架构结果、风险、影响、价值或沟通问题。 | 决定范围、需求、视点、沟通和方案评价准则。 | C220-Part1e-Architecture Development Method.md | [[architecture-viewpoint(架构视点)]]、[[architecture-scope(架构范围)]] | single-source | 与视点保持问题和表达机制的区分。 |
| [[target-architecture(目标架构)]] | 企业为实现愿景、目标和需求而计划达到的未来架构状态。 | 阶段 A 给出轮廓，阶段 B–D 形成详细域目标。 | C220-Part1e-Architecture Development Method.md | [[baseline-architecture(基线架构)]]、[[transition-architecture(过渡架构)]] | single-source | 不等同于最终实施计划。 |
| [[technology-architecture(技术架构)]] | 描述实现业务、数据和应用需求所需技术服务、组件、平台和标准的架构域。 | 阶段 D 形成技术基线、目标、差距和路线图组件。 | C220-Part1e-Architecture Development Method.md | [[application-architecture(应用架构)]]、[[solution-building-block(解决方案构建块)]] | single-source | 不把架构退化为产品清单。 |
| [[trade-off-analysis(权衡分析)]] | 依据准则比较候选方案或冲突视图并明确得失的决策活动。 | 支持阶段 B–E 的目标架构和解决方案选择。 | C220-Part1e-Architecture Development Method.md | [[architecture-alternative(架构替代方案)]]、[[architecture-principles(架构原则)]] | single-source | 记录准则、后果和决策理由。 |
| [[transition-architecture(过渡架构)]] | 基线和最终目标之间可运行、完整且有业务结果的中间架构状态。 | 让大型转型按能力增量和里程碑分步交付。 | C220-Part1e-Architecture Development Method.md | [[baseline-architecture(基线架构)]]、[[target-architecture(目标架构)]] | single-source | 不等同于任意项目阶段或临时环境。 |
| [[value-realization(价值实现)]] | 部署后验证预期价值是否转化为实际业务成果的持续过程。 | 阶段 H 监测结果并触发改进或架构变更。 | C220-Part1e-Architecture Development Method.md | [[business-value(业务价值)]]、[[architecture-change-management(架构变更管理)]] | single-source | 与事前价值估算保持边界。 |
| [[value-stream(价值流)]] | 为客户或利益相关者创造总体结果的一组端到端增值活动。 | 阶段 A/B 连接价值对象、利益相关者和业务能力。 | C220-Part1e-Architecture Development Method.md | [[business-capability(业务能力)]]、[[business-value(业务价值)]] | single-source | 不等同于单一业务流程。 |
| [[work-package(工作包)]] | 为消除相关差距并交付能力增量而组合的一组逻辑变更。 | 阶段 E/F 连接差距、解决方案、项目和路线图。 | C220-Part1e-Architecture Development Method.md | [[architecture-roadmap(架构路线图)]]、[[solution-building-block(解决方案构建块)]] | single-source | 与 SBB 或项目实体保持区分。 |

## 概念集群

- 方法及治理：架构开发周期、架构范围、企业架构能力、架构原则、架构治理、企业连续统一体、架构存储库。
- 愿景及状态：架构愿景、利益相关者关注点、架构视点、基线架构、目标架构、过渡架构。
- 架构域：业务能力、价值流、业务架构、数据架构、应用架构、技术架构。
- 构建及评估：架构构建块、解决方案构建块、架构替代方案、权衡分析、差距分析。
- 交付及演进：架构路线图、工作包、实施计划、迁移计划、业务价值、价值实现、架构变更管理、架构需求管理。
