# 查询(query)工作流 — 参考

依据 wiki 回答问题，并可选择将答案归档为新页面的详细协议。

## 触发条件

用户询问 wiki 领域内的问题。无需特殊命令——任何问题都会触发此工作流。

## 核心流程

### 步骤 0：偏好与搜索门控

使用 `references/config/extend-schema.md` 加载 `EXTEND.md` 偏好。如果不存在偏好文件，先完成首次偏好设置。

如果 `bm25.mode: auto_prompt`，检查配置的阈值。如果达到阈值且尚未初始化 BM25，询问是否初始化。用户同意后，遵循 `references/workflows/bm25.md`。

### 步骤 1：通过索引导航

读取 `wiki/index.md`。对于概念、关系、分类或全局性问题，在选择页面前还要读取 `wiki/concept-table.md`。找出可能与查询相关的页面。如果配置了 BM25，在读取索引后将其作为额外的候选查找工具，而不是索引的替代品。

如果已启用 BM25，在读取索引后使用它：

```bash
python3 scripts/wiki_fts.py stats
python3 scripts/wiki_fts.py search "{user question or extracted query terms}" --limit 10
```

如果 `stats` 报告 `Fresh: no`，搜索前运行 `python3 scripts/wiki_fts.py rebuild`。如果重建失败且 `fallback_to_rg: true`，继续使用 `rg` 和 `wiki/index.md`。

BM25 只返回候选文本块。不要仅根据摘要片段回答；打开返回的页面并阅读全文中的相关上下文。

### 步骤 2：读取相关页面

读取已确定的页面。如果页面引用了其他可能相关的页面，也继续读取。获得足够上下文或已经读取 15 个以上页面时停止；达到后者时，使用已有信息完成工作。

如果 BM25 不可用、已过期或没有返回有用结果，并且 `fallback_to_rg: true`，则回退到 `rg` 和 `wiki/index.md`。

### 步骤 3：综合答案

组织答案时：

- 直接回答用户的问题
- 使用 wiki 页面内联引用：`[Page Title](wiki/path/to/page.md)`（页面标题可按实际内容替换）
- 标明置信度：高（多个来源相互印证）、中（单一来源）、低（推断）
- 如果 wiki 中没有足够信息完整作答，明确指出

### 步骤 4：归档决策

回答后评估：这个答案是否是值得保存的有价值成果？

**值得归档的信号**：

- 用户可能再次查看的比较或分析
- 在现有概念之间发现了新联系
- 综合了 3 个以上来源
- 答案填补了 wiki 的覆盖缺口

**不值得归档的情形**：

- 简单事实查询
- 关于 wiki 结构的澄清问题
- 琐碎或一次性查询

如果值得归档，询问用户：“这份分析值得保留。是否归档为 `wiki/{type}/{slug}.md`？”

如果用户同意：

1. 使用正确的 frontmatter 创建页面
2. 添加与相关页面之间的双向引用
3. 如果归档的答案创建、重命名、合并、拆分或实质性修订了持久概念，更新 `wiki/concept-table.md`
4. 更新 `wiki/index.md`
5. 向 `wiki/log.md` 追加：

   ```text
   ## [{date}] query-filed | {title}
   - 问题：{original question}
   - 归档位置：wiki/{type}/{slug}.md
   - 相关页面：{list}
   ```

## 答案格式

根据问题类型调整输出格式：

| 问题类型 | 格式 |
| --- | --- |
| “X 是什么？” | 1–3 段文字说明 |
| “比较 X 和 Y” | 以比较维度为行的 Markdown 表格 |
| “关于 X，我们知道什么？” | 带来源引用的结构化摘要 |
| “关于 X 有哪些开放问题？” | 带置信度评估的编号列表 |
| “总结 X 的现状” | 按小节组织、包含关键主张的概览 |
| “X 的时间线” | 按时间顺序排列的列表或表格 |

## Wiki 无法回答时

如果 wiki 缺少信息：

1. 明确说明缺少什么
2. 建议可能填补缺口的来源（网络搜索、具体文档）
3. 可选择创建一个记录知识缺口的占位页面：

   ```yaml
   ---
   title: "{topic}"
   type: concept
   created: {date}
   updated: {date}
   sources: []
   tags: [stub, needs-sources]
   ---
   ```
