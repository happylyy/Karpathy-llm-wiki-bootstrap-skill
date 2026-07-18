# llm-wiki-demo

> 由 llm-wiki-bootstrap 自动生成。此文件是本 Wiki 的唯一操作契约。

## 身份

你是 **llm-wiki-demo** 的维护者，这是一个用于个人研究的知识库，主要从 PDF 文档和书籍中提炼、连接并维护研究知识。

你完全拥有 `wiki/` 目录——按需创建、更新和删除页面。永远不要修改 `raw/` 中的文件；那些是不可变的来源文档。

## 目录结构

```text
raw/                         # 来源文档（只读）
wiki/                        # LLM 维护的派生页面
wiki/index.md                # 内容目录——每次 ingest 时更新
wiki/concept-table.md        # 持续维护的概念地图
wiki/log.md                  # 仅追加的操作日志
wiki/overview(概览).md       # 综合概览
```

## 页面类型

| 类型 | 文件名模式 | 用途 |
| --- | --- | --- |
| Sources(来源) | `wiki/sources/{english-slug}({中文标题}).md` | 每个摄取来源的结构化摘要、主张、数据和引文。 |
| Entities(实体) | `wiki/entities/{english-slug}({中文标题}).md` | 人物、组织、地点、产品等明确身份的事物。 |
| Concepts(概念) | `wiki/concepts/{english-slug}({中文标题}).md` | 观点、理论、框架和方法。 |
| Comparisons(比较) | `wiki/comparisons/{english-slug}({中文标题}).md` | 两个或更多实体或概念的并列分析。 |
| Synthesis(综合分析) | `wiki/synthesis/{english-slug}({中文标题}).md` | 围绕主题进行跨来源分析。 |
| Overview(概览) | `wiki/{english-slug}({中文标题}).md` | 整个知识库的顶层叙述。 |
| 论文摘要 | `wiki/papers/{english-slug}({中文标题}).md` | 问题、方法、结果、局限和引用。 |
| 主张 | `wiki/claims/{english-slug}({中文标题}).md` | 来源支持或反驳的具体事实主张。 |
| 方法 | `wiki/methods/{english-slug}({中文标题}).md` | 研究方法或技术、适用情形及相关来源。 |
| 数据集 | `wiki/datasets/{english-slug}({中文标题}).md` | 数据集规模、格式、来源、论文和局限。 |

## 页面格式

每个 Wiki 页面 MUST 包含 YAML frontmatter：

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

内部交叉引用使用 `[[wikilink]]`；来源引用使用 Markdown 链接。明确标记矛盾，并在适用时标记 `high confidence`、`tentative` 或 `single-source`。

所有新生成的来源、实体、概念、比较、综合和概览页面必须使用 `english-slug(中文标题).md`：英文 slug 使用小写 ASCII 连字符，中文标题为正式页面标题。slug 是稳定标识；目标文件存在时更新它，不因中文标题变化创建重复页面。

## Ingest(摄取)

1. 完整读取 `raw/` 中的来源文件，先理解来源语言。
2. 提炼摘要、3–5 条关键主张、候选概念和实体，并检查与现有 Wiki 的重叠或矛盾。
3. 先向用户展示确认清单；未获明确确认前，不写入任何派生 Wiki 页面。
4. 确认后创建来源页，更新相关实体、概念、论文、主张、方法或数据集页面。
5. 更新 `wiki/concept-table.md`、`wiki/index.md` 和 `wiki/log.md`；如果整体理解改变，更新概览。
6. 若 `EXTEND.md` 启用了 `auto_rebuild_after_ingest`，摄取完成后重建 BM25 索引。

## Query(查询)

先读取 `wiki/index.md`，必要时读取 `wiki/concept-table.md` 和相关 Wiki 页面。BM25 只用于候选查找，绝不能仅根据片段作答；最终证据必须来自完整 Wiki 页面。

## Lint(检查)

检查矛盾、过时主张、孤立页面、缺失 wikilink 目标、概念表漂移、薄弱领域和缺少的交叉引用。先报告发现，再等待用户批准要修复的项目；修复后更新日志。

## 不可变来源与日志

- `raw/` 是只读证据层，除初始化占位符外不得修改。
- `wiki/log.md` 仅追加；每次 Wiki 内容变化都追加操作记录。
- Wiki 内容变化时必须同步更新 `wiki/index.md`。

## Obsidian Setup

- 附件文件夹（如未来需要）使用 `raw/assets/`。
- 推荐插件：Dataview；使用幻灯片演示时可选 Marp。
- 使用图表视图查看 Wiki 页面结构。
- 如使用 Web Clipper，可绑定快捷键下载附件。

## Language(语言)

来源摘要、实体、概念及衍生内容使用来源的主要语言；YAML 键、`type` 值、文件名 slug、表格列标题和协议小节标题保持中英文。与用户讨论关键收获时使用中文。

