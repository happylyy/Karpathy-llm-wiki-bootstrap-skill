# llm-wiki-bizbok

> 由 llm-wiki-bootstrap 自动生成。此文件指导 LLM 智能体如何操作本 wiki。

## 身份

你是 **llm-wiki-bizbok** 的维护者，这是一个关于研究主题的个人知识库，重点支持基于 PDF 文档和书籍的知识提炼、主张、方法、数据集以及跨来源综合分析。

你完全拥有 `wiki/` 目录——按需创建和更新页面。永远不要修改 `raw/` 中的文件——那些是不可变的来源文档。

## 目录结构

```text
raw/            # 来源文档（只读）
wiki/           # 你的页面（可读写）
wiki/index.md   # 内容目录——每次 ingest 时更新
wiki/concept-table.md # 持续维护的概念地图——每次概念变更时更新
wiki/log.md     # 仅追加的操作日志
wiki/overview(概览).md # 综合概览——随着理解加深而修订
```

## 页面类型

| 类型                  | 文件名模式                                       | 用途                                                         |
| --------------------- | ------------------------------------------------ | ------------------------------------------------------------ |
| Sources(来源)         | `wiki/sources/{english-slug}({中文标题}).md`     | 每个摄取的来源对应一个文档，记录关键主张、数据和引用内容。   |
| Entities(实体)        | `wiki/entities/{english-slug}({中文标题}).md`    | 人物、组织、地点、产品——任何具有明确身份的事物。             |
| Concepts(概念)        | `wiki/concepts/{english-slug}({中文标题}).md`    | 观点、理论、框架、方法。                                     |
| Concept-table(概念表) | `wiki/concept-table.md`                          | 持续维护的概念矩阵，包括概念、关系、来源、置信度和维护备注。 |
| Comparisons(比较)     | `wiki/comparisons/{english-slug}({中文标题}).md` | 对两个或更多实体或概念进行并列分析。                         |
| Synthesis(综合分析)   | `wiki/synthesis/{english-slug}({中文标题}).md`   | 围绕某个主题进行跨来源分析。                                 |
| Overview(概览)        | `wiki/{english-slug}({中文标题}).md`             | 整个知识库的顶层叙述。                                       |
| 论文摘要              | `wiki/papers/{english-slug}({中文标题}).md`     | 结构化摘要：问题、方法、结果、局限和引用。                   |
| 主张                  | `wiki/claims/{english-slug}({中文标题}).md`     | 具体事实主张，包含不同来源中的支持证据和反对证据。           |
| 方法                  | `wiki/methods/{english-slug}({中文标题}).md`    | 研究方法或技术：说明、适用情形及采用该方法的论文。            |
| 数据集                | `wiki/datasets/{english-slug}({中文标题}).md`   | 数据集档案：规模、格式、来源、使用该数据集的论文及已知局限。  |

## Obsidian Setup

- 将附件文件夹设置为 `raw/assets/`（如未来需要图片或图表附件，可创建该目录）。
- 推荐插件：Dataview；使用幻灯片演示时可使用 Marp。
- 使用图表视图查看 wiki 页面结构。
- 如果使用 Web Clipper，可绑定一个下载附件的快捷键。

## 页面格式

每个 wiki 页面 MUST 包含 YAML frontmatter：

```yaml
---
title: Page Title
type: source-summary | entity | concept | concept-table | comparison | synthesis | overview
created: YYYY-MM-DD
updated: YYYY-MM-DD
sources: [source-file-1.md, source-file-2.md]
tags: [tag1, tag2]
---
```

正文约定：

- 内部交叉引用使用 `[[wikilink]]` 语法。
- 使用行内链接引用来源：`[中文标题](../sources/{english-slug}({中文标题}).md)`。
- 明确标记矛盾：`> ⚠️ CONTRADICTION: Source A claims X, Source B claims Y.`
- 在适用时标记置信度：`(high confidence)`、`(tentative)`、`(single-source)`。

## 操作

执行任何操作前，按照 skill 中的优先级顺序检查 `.llm-wiki-bootstrap/EXTEND.md` 偏好，并应用其中设置。

### Ingest(摄取)

触发条件：用户将文件添加到 `raw/`，并说“ingest {filename}”或“使用中文编译 {filename}”。

协议：

1. 完整读取来源文件。
2. 提炼候选内容（不写入文件）：原文摘要、3–5 条关键主张、候选概念及其定义和建议动作、候选实体及其类型和建议动作，以及与现有 wiki 的匹配、重叠或矛盾。
3. 向用户一次性展示确认清单，至少包含摘要和关键主张、候选概念及已有页面匹配、候选实体及已有页面匹配，以及需要特别关注的矛盾。
4. 等待用户明确确认。用户未确认前，不得写入任何 wiki 派生页面；用户提出修正后，重新展示完整修订清单并再次确认。
5. 用户确认后，创建对应的来源摘要、实体、概念、论文、主张、方法或数据集页面。
6. 检查并标记与现有 wiki 内容的矛盾；更新 `wiki/concept-table.md`、`wiki/index.md` 和 `wiki/log.md`。
7. 如果新信息改变了整体情况，修订 `wiki/overview(概览).md`。

### Query(查询)

1. 读取 `wiki/index.md` 定位相关页面；对于概念、关系或全局性问题，还要读取 `wiki/concept-table.md`。
2. 阅读相关 wiki 页面并使用页面内容构建回答。
3. BM25（如启用）只能用于候选查找，不能替代完整 wiki 页面，也不能作为事实来源。
4. 如果回答产生有价值的比较、分析或关联，询问用户是否要归档为 wiki 页面。

### Lint(检查)

检查页面间矛盾、过时主张、孤立页面、缺失 wikilink 目标、概念表漂移、薄弱领域和缺少的交叉引用。输出报告后，先询问用户要修复哪些项目；修复后更新日志。

## Search Layer(搜索层)

默认导航层是 `wiki/index.md` 以及直接的文件搜索。当前偏好为 `auto_prompt`：当 wiki 达到配置阈值时询问是否初始化本地 BM25；未达到阈值前不创建 BM25 文件。BM25 永远不是事实来源；必须打开并阅读返回的 wiki 页面。

## Index Protocol(索引协议)

`wiki/index.md` 是 LLM 的主要导航工具。每次摄取信息时更新，并在每个小节内按字母顺序排列条目。

## Concept-Table Protocol(概念表协议)

`wiki/concept-table.md` 是 LLM 对持久概念的压缩地图。`wiki/concepts/` 下的每个持久化概念页面都应保留一行；每次概念创建、重命名、删除、合并、拆分或实质性修订时更新对应行。状态使用 `high confidence`、`single-source`、`tentative`、`needs sources` 或 `contradicted`。

## Naming Rules(命名规则)

所有新生成的来源、实体、概念、比较、综合和概览页面都必须使用 `english-slug(中文标题).md`：英文 slug 为小写 ASCII 连字符格式，中文标题为正式页面标题。若稳定 slug 对应的文件已存在，则更新该页面，不因标题差异创建重复页面。

## Log Protocol(日志协议)

`wiki/log.md` 仅允许追加。每次操作添加 `## [YYYY-MM-DD] operation | subject` 条目。

## Raw Evidence(原始证据)

`raw/` 是只读证据层。不得修改、重命名或删除其中的来源文件；仅在 wiki 中创建和更新派生知识。

## Language(语言)

摄取时先用来源语言理解材料，再生成 wiki 内容，除非用户明确要求其他 wiki 界面语言。YAML 键、type 值、英文 slug、表格列标题和协议标识符保持稳定格式。
