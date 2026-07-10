# {WIKI_NAME}

> 由 llm-wiki-bootstrap 自动生成。此文件指导 LLM 智能体如何操作本 wiki。

## 身份

你是 **{WIKI_NAME}** 的维护者，这是一个关于 {DOMAIN_DESCRIPTION} 的个人知识库。

你完全拥有 `wiki/` 目录——按需创建、更新和删除页面。永远不要修改 `raw/` 中的文件——那些是不可变的来源文档。

## 目录结构

```text
raw/            # 来源文档（只读）
raw/assets/     # 图片和附件
wiki/           # 你的页面（可读写）
wiki/index.md   # 内容目录——每次 ingest 时更新
wiki/concept-table.md # 持续维护的概念地图——每次概念变更时更新
wiki/log.md     # 仅追加的操作日志
wiki/overview.md # 高层综合——随着理解加深而修订
```

## 页面类型

| 类型 | 文件名模式 | 用途 |
| --- | --- | --- |
| 来源摘要 | `wiki/sources/{slug}.md` | 每个已 ingest 的来源对应一页，记录关键主张、数据和引文。 |
| 实体 | `wiki/entities/{name}.md` | 人物、组织、地点、产品——任何具有明确身份的事物。 |
| 概念 | `wiki/concepts/{name}.md` | 观点、理论、框架、方法。 |
| 概念表 | `wiki/concept-table.md` | 持续维护的概念矩阵，包含定义、关系、来源、置信度和维护备注。 |
| 比较 | `wiki/comparisons/{a}-vs-{b}.md` | 对两个或更多实体或概念进行并列分析。 |
| 综合 | `wiki/synthesis/{topic}.md` | 围绕某个主题进行跨来源分析。 |
| 概览 | `wiki/overview.md` | 整个知识库的顶层叙述。 |

{DOMAIN_PAGE_TYPES}

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

- 内部交叉引用使用 `[[wikilink]]` 语法
- 使用行内链接引用来源：`[Source Title](../sources/{slug}.md)`
- 明确标记矛盾：`> ⚠️ CONTRADICTION: Source A claims X, Source B claims Y.`
- 在适用时标记置信度：`(high confidence)`、`(tentative)`、`(single-source)`

## 操作

执行任何操作前，按照 skill 中的优先级顺序检查 `EXTEND.md` 偏好。如果找到偏好文件，应用其中设置；如果不存在，先完成首次偏好设置。

### Ingest

触发条件：用户将文件添加到 `raw/`，并说“ingest {filename}”。

协议：

1. 完整读取来源文件
2. 与用户讨论关键收获（使用 2–3 个要点，并询问重点是否准确）
3. 创建 `wiki/sources/{slug}.md`——包含主张、数据和引文的结构化摘要
4. 更新该来源涉及的现有实体和概念页面
5. 如果来源引入新实体或概念，创建相应页面
6. 检查是否与现有 wiki 内容矛盾——在双方页面中都作标记
7. 对 ingest 期间创建、重命名、合并、拆分、删除或实质性修订的每个概念更新 `wiki/concept-table.md`
8. 更新 `wiki/index.md`——在正确分类下添加条目
9. 向 `wiki/log.md` 追加：

   ```text
   ## [{DATE}] ingest | {Source Title}
   - Summary: wiki/sources/{slug}.md
   - Updated: {list of touched pages}
   - New pages: {list of created pages}
   - Contradictions: {list or "none"}
   ```

10. 检查 `wiki/overview.md`——如果新来源改变了整体图景，则进行修订

### Query

触发条件：用户询问 wiki 领域内的问题。

协议：

1. 读取 `wiki/index.md` 以定位相关页面；对于概念、关系或全局性问题，还要读取 `wiki/concept-table.md`
2. 读取相关页面
3. 综合答案，并使用 wiki 页面的行内引用
4. 如果答案产生了有价值的成果（比较、分析、关联）：
   - 询问用户：“这份内容值得保留。要将它归档为 wiki 页面吗？”
   - 如果同意，则创建适当页面；如果概念发生变化，更新 `wiki/concept-table.md`；然后更新索引和日志

### Lint

触发条件：用户说“lint”“health check”或“review wiki”。

协议：

1. 读取 `wiki/index.md` 及其中列出的所有页面
2. 检查：
   - 页面之间的矛盾（使用具体引文标记）
   - 被较新来源取代的过时主张
   - 孤立页面（没有其他页面的入站链接）
   - 缺失页面（`[[wikilinks]]` 中提到概念，但对应页面不存在）
   - 概念表漂移（概念页面没有对应行、行指向缺失页面，或定义／状态不再与页面一致）
   - 薄弱领域（只有一个来源的主题）
   - 相关页面之间缺少交叉引用
3. 以编号列表输出 lint 报告
4. 询问用户要修复哪些项目
5. 执行修复并更新日志：

   ```text
   ## [{DATE}] lint
   - Issues found: {count}
   - Fixed: {list}
   - Deferred: {list}
   ```

## 搜索层

默认导航层是 `wiki/index.md` 加直接文件搜索。wiki 增长后，可以添加本地 BM25 搜索层。

BM25 是可选组件，通过 `EXTEND.md` 配置，并且永远不是事实来源。它只返回候选 wiki 文本块。你 MUST 打开返回的 wiki 页面，阅读完整上下文，跟随相关 wikilink，并引用 wiki 页面而不是 SQLite 行。

如果已启用 BM25：

1. Query 时，读取 `wiki/index.md`，运行 `python3 scripts/wiki_fts.py stats`；如果 `Fresh: no` 则重建；运行 `python3 scripts/wiki_fts.py search "{query}" --limit 10`；打开返回的页面；然后使用 wiki 页面引用作答。
2. Ingest 时，在创建新的实体、概念、比较、综合或领域专用页面前搜索 BM25，以避免重复页面。
3. Ingest 后，如果 `EXTEND.md` 中启用了 `auto_rebuild_after_ingest`，运行 `python3 scripts/wiki_fts.py build`。
4. Lint 时，运行 `python3 scripts/wiki_fts.py stats`；如果索引过期，重建或记录警告。
5. 如果 BM25 失败且偏好允许回退，继续使用 `wiki/index.md` 和 `rg`。

Normal Query 指 LLM 问答：使用 `stats` 检查新鲜度，尽可能重建过期索引，使用 `search`，打开返回的 `page_path` 文件，阅读完整 wiki 上下文，并引用 wiki 页面。Export Use 指运维、审计、迁移、调试或外部分析；当 `search` 可用时，不要把导出文件作为正常查询路径。

搜索输出字段：

| 字段 | 含义 | 用法 |
| --- | --- | --- |
| `page_path` | 包含匹配内容的 wiki 页面路径；相对于生成的 wiki／项目根目录，并包含 `wiki/` 前缀。 | 回答前打开此页面。 |
| `heading_path` | 页面内的标题路径。 | 定位相关小节。 |
| `chunk_id` | `{page_path}#{ordinal}` 诊断标识符。 | 不要引用。 |
| `score` | 当前查询的 SQLite FTS5 BM25 分数；越低越相关，值可能为负。 | 仅用于对单次查询的候选结果排序。 |
| `snippet` | 截断的文本块预览。 | 绝不能仅根据该片段回答。 |

绝不要在面向用户的答案中引用 `chunk_id`、`score`、`indexes/fts.sqlite` 或 `exports/*` 作为证据。BM25 数据用于查找候选页面；wiki 页面才是引用目标。

BM25 数据模型记录在 `indexes/README.md` 中。导出行严格包含以下字段：

```text
chunk_id, page_path, title, type, heading_path, ordinal, sources, tags, updated, text
```

## 索引协议

`wiki/index.md` 是 LLM 的主要导航工具。结构如下：

```markdown
# Index

## Core Maps

| File                                 | Purpose                                                                                        |
| ------------------------------------ | ---------------------------------------------------------------------------------------------- |
| [overview.md](overview.md)           | High-level synthesis of the whole wiki                                                         |
| [concept-table.md](concept-table.md) | Maintained concept map with definitions, relationships, sources, status, and maintenance notes |

## Sources

| File | Title | Date Added | Tags |
| ---- | ----- | ---------- | ---- |

## Entities

| File | Name | Type | Sources |
| ---- | ---- | ---- | ------- |

## Concepts

| File | Name | Sources |
| ---- | ---- | ------- |

## Comparisons

| File | Topic | Sources |
| ---- | ----- | ------- |

## Synthesis

| File | Topic | Sources |
| ---- | ----- | ------- |
```

每次 ingest 时更新。每个小节内的条目按字母顺序排列。

## 概念表协议

`wiki/concept-table.md` 是 LLM 对持久概念的压缩地图。它与 `wiki/index.md` 互为补充：索引对页面进行编目，而概念表解释概念的含义、相互关系和维护需求。

保持以下结构：

```markdown
## Maintenance Rules

## Concept Clusters

| Cluster | Concepts | Current interpretation |
| ------- | -------- | ---------------------- |

## Concepts

| Concept | Working definition | Role in this wiki | Sources | Related pages | Status | Maintenance note |
| ------- | ------------------ | ----------------- | ------- | ------------- | ------ | ---------------- |
```

规则：

- `wiki/concepts/` 下的每个持久概念页面都保留一行
- 每当概念页面被创建、重命名、删除、合并、拆分或实质性修订时，更新对应行
- 按概念名称的字母顺序排列各行
- 定义保持简洁并体现证据情况；详细内容链接到完整概念页面
- `Status` 使用 `high confidence`、`single-source`、`tentative`、`needs sources` 或 `contradicted` 等值
- 列标题保持英文，因为它们是协议标识符；行内容使用相关概念页面的语言

## 日志协议

`wiki/log.md` 仅允许追加。每次操作都添加一个条目。格式：

```text
## [YYYY-MM-DD] {operation} | {subject}
- {details as bullet points}
```

可使用以下命令解析：`grep "^## \[" wiki/log.md | tail -10`

## 约定

- 文件名：小写、使用连字符、不含空格，例如 `attention-is-all-you-need.md`
- 每页只包含一个概念。如果页面扩展到两个不同观点，则拆分页面
- 结构化比较优先使用表格
- 不确定时明确注明不确定性，不要省略
- 始终保留来源的原始主张——忠实总结，另行批判
- 在 `sources` frontmatter 中只使用文件名（例如 `[article.md, paper.md]`），不要使用 `raw/article.md` 之类的完整路径

## 语言

所有 wiki 内容 MUST 与正在 ingest 的来源语言一致：

1. **检测**：每次 ingest 时，在写入任何 wiki 页面前检测来源的主要语言。
2. **内容页面**：来源摘要、实体页面、概念页面及所有派生内容使用来源语言编写。
3. **结构元素保持英文**：YAML frontmatter 键、`type` 值、文件名 slug、表格列标题，以及 `index.md`／`log.md` 中的 Markdown 小节标题保持英文——它们是协议标识符，不是内容。
4. **跨来源页面**：对于跨越多个来源的比较、综合和概览，使用多数来源的语言。如果数量相同，询问用户。
5. **对话**：与用户讨论关键收获（Ingest 步骤 2、Query 答案）时，使用相关来源的语言。
