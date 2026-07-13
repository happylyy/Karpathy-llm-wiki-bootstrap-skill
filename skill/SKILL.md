---
name: llm-wiki-bootstrap
description: >
  引导创建和操作 LLM Wiki：一个持久化的 Markdown 知识库，其中包含不可变的原始资料、
  由 LLM 维护的 wiki、作为操作契约的 SCHEMA.md、精简的运行时指针文件、EXTEND.md
  偏好配置，以及可选的本地 BM25 搜索。当用户要求创建或引导建立 LLM wiki、摄取资料、
  查询或检查 wiki、配置 EXTEND.md 偏好，或为 LLM Wiki 设置 BM25/全文搜索时使用。
version: 0.1.0
---

# LLM Wiki 引导

构建和维护个人 LLM Wiki：原始证据在 `raw/` 中保持不可变，持久知识被编译到 `wiki/` 中，而 `SCHEMA.md` 是所生成 wiki 的唯一操作契约。

本文档有意保持简短。仅加载用户所请求操作对应的详细参考资料。

## 操作模型

- 将 `SCHEMA.md` 作为每个所生成 wiki 中的唯一事实来源。
- 将 `wiki/concept-table.md` 作为持续维护的概念图：它通过汇总持久概念、关系、来源、状态和维护说明，对 `wiki/index.md` 形成补充。
- 将 `CLAUDE.md`、`AGENTS.md` 和 `.github/copilot-instructions.md` 保持为指向 `SCHEMA.md` 的精简指针；绝不在其中复制操作规则。
- 将 `raw/` 视为只读证据。仅在 `wiki/` 下创建和更新派生知识。
- 在执行引导创建（bootstrap）、摄取（ingest）、查询（query）、检查（lint）或 BM25 工作之前应用 `EXTEND.md` 中的偏好。 
- 仅询问缺失的决策，并尽可能将设置问题合并到一次用户提问中。
- 优先采用渐进式披露：读取能够完成当前任务的最小参考文件。

## 意图路由

| 用户意图                         | 执行操作                                                                                  | 参考资料                                                               |
| -------------------------------- | ----------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| 创建或引导建立新的 wiki          | 运行偏好预检，收集设置答案，然后生成骨架和种子文件。                                      | `references/workflows/bootstrap.md`                                    |
| 摄取一个或多个资料来源           | 运行偏好预检，检查可选的 BM25 门控，然后将来源知识编译到 `wiki/` 中。                      | `references/workflows/ingest.md`                                       |
| 根据 wiki 回答领域问题           | 运行偏好预检，从 `wiki/index.md` 导航，仅将 BM25 用作候选查找器，然后引用 wiki 页面。      | `references/workflows/query.md`                                        |
| 检查 wiki 健康状况或一致性       | 运行偏好预检，扫描结构和内容，报告发现，然后仅修复获准的项目。                            | `references/workflows/lint.md`                                         |
| 配置或使用 BM25 搜索             | 加载偏好，在初始化前询问，创建本地搜索文件，执行冒烟测试，并记录结果。                    | `references/workflows/bm25.md`                                         |
| 配置偏好                         | 使用架构和模板定位或创建 `EXTEND.md`。                                                     | `references/config/extend-schema.md`、`references/templates/extend.md` |

## 偏好预检

在执行引导创建、摄取、查询、检查或 BM25 工作之前，读取 `references/config/extend-schema.md`，并按照其中的查找顺序使用第一个可用的 `EXTEND.md`。如果不存在，则运行首次偏好设置，并根据 `references/templates/extend.md` 创建一个偏好文件，然后再继续。

在会话中首次使用时，简要说明当前启用的是哪个偏好文件。不得静默使用默认值。

## 参考资料加载规则

- 对于引导创建，读取 `references/workflows/bootstrap.md`，然后仅在创建相应文件时加载各个模板。
- 对于摄取、查询和检查，先读取匹配的工作流文件；仅当偏好或用户请求需要搜索行为时，才读取 `references/workflows/bm25.md`。
- 对于骨架生成，读取 `references/templates/schema.md`，并根据需要注入 `references/templates/domain-page-types.md` 中的领域片段。
- 对于指针文件，读取 `references/templates/agent-pointer.md`，并保持所生成文件的精简性。
- 对于 BM25 初始化，仅在用户批准初始化之后读取 `references/templates/wiki_fts.py` 和 `references/templates/bm25-readme.md`。

## 包布局规则

- 如果由 skill 自身拥有的可运行辅助工具需要从已安装的 skill 包中执行，则将它们放入 `scripts/`。
- 将生成输出所用的模板放入 `references/templates/`，即使生成的文件在复制到用户的 wiki 后将成为可执行文件。
- 将较长的过程文档放入 `references/workflows/`，将配置架构放入 `references/config/`。
- 在此 skill 中，`references/templates/wiki_fts.py` 是生成 wiki 中 `scripts/wiki_fts.py` 的模板；skill 不会就地执行它。

## 硬性规则

- 未经用户明确批准，绝不覆盖现有 wiki。
- 除了在引导创建期间创建 `.gitkeep` 等空骨架占位符之外，绝不修改 `raw/` 中的文件。
- 绝不直接根据 BM25 片段作答；必须先打开并阅读返回的 wiki 页面。
- 摄取时首先使用来源语言理解材料，然后使用中文理解并生成wiki非用户要求使用不同的 wiki 语言。
- 每当 wiki 内容发生变化时，更新 `wiki/index.md` 并追加写入 `wiki/log.md`。
- 如果搜索索引重建失败，保留 wiki 编辑，记录失败，并回退到 `wiki/index.md` 加文本搜索。

## 核心输出

成功的引导创建会生成一个包含以下内容的 wiki 根目录：

```text
raw/
wiki/index.md
wiki/concept-table.md
wiki/log.md
wiki/overview.md
SCHEMA.md
.gitignore
```

可选输出取决于设置答案和偏好：运行时指针文件、`.vscode/settings.json`、`scripts/wiki_fts.py`、`indexes/` 和 `exports/`。
