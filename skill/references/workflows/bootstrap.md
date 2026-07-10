# Bootstrap 工作流 — 参考

仅当用户希望创建新的 LLM Wiki 脚手架时使用此工作流。
在阶段 1 之前，按照 `references/config/extend-schema.md` 查找偏好并完成首次偏好设置。

## 目标

创建一个可立即使用的 LLM Wiki，其中包含不可变的来源层、由 LLM 维护的 wiki 层、作为操作契约的 `SCHEMA.md`、可选的运行时指针，以及用户选择的编辑器和搜索配置。

## 阶段 1：收集需求

阻塞条件：创建文件前必须完成此阶段。

在一次用户提示中询问所有问题：

| 标题 | 问题 | 备注 |
| --- | --- | --- |
| 领域 | 这个 wiki 的主题是什么？ | 选项：研究主题；书籍／媒体；个人（目标、健康、学习）；企业／团队；其他。 |
| Wiki 名称 | wiki 根目录使用什么短名称？ | 自由文本。建议使用 `{domain}-wiki`，例如 `ml-wiki`、`lotr-wiki` 或 `health-wiki`。 |
| 运行时 | 哪些运行时会读取此 wiki？ | 多选：Claude Code、OpenAI Codex、Copilot（VS Code）、其他／通用。 |
| 编辑器 | 浏览 wiki 时主要使用哪个编辑器？ | 选项：Obsidian（推荐）、VS Code、其他／纯文件。 |
| 来源类型 | 你会添加哪些类型的来源？ | 多选：网页文章、PDF／论文、书籍、会议记录／转录、个人笔记／日志、图片／图表、数据文件、其他。 |
| 输出位置 | 在哪里创建 wiki？ | 当前目录或自定义绝对路径。 |

保存这些回答供后续阶段使用。如果自定义输出位置含义不明确，写入文件前再询问一个后续问题。

## 阶段 2：创建目录结构

在 `{wiki-root}/` 下创建以下基础目录树：

```text
{wiki-root}/
├── raw/
│   └── assets/             # 仅在选择图片／图表来源时创建
├── wiki/
│   ├── index.md
│   ├── concept-table.md
│   ├── log.md
│   └── overview.md
├── SCHEMA.md
├── {pointer-files}
└── .gitignore
```

条件输出：

| 条件 | 添加内容 |
| --- | --- |
| 来源类型包含图片／图表 | `raw/assets/` |
| 选择了任意来源类型 | `raw/.gitkeep` |
| 编辑器是 Obsidian | 不要创建 `.obsidian/`；Obsidian 会自行创建。 |
| 编辑器是 VS Code | 创建包含适合 Markdown 的默认设置的 `.vscode/settings.json`。 |
| 运行时包含 Claude Code | `CLAUDE.md` 指针。 |
| 运行时包含 OpenAI Codex | `AGENTS.md` 指针。 |
| 运行时包含 Copilot（VS Code） | `.github/copilot-instructions.md` 指针。 |

使用 `references/templates/gitignore.md` 创建 `.gitignore`。

写入现有路径前先检查其内容。如果生成的文件会覆盖用户内容，请求批准或选择其他 wiki 根目录。

## 阶段 3：生成 `SCHEMA.md`

使用 `references/templates/schema.md` 写入 `{wiki-root}/SCHEMA.md`。

模板变量：

| 变量 | 来源 |
| --- | --- |
| `{WIKI_NAME}` | Wiki 名称回答。 |
| `{DOMAIN_DESCRIPTION}` | 将领域回答扩展成 1–2 个清晰句子。 |
| `{SOURCE_TYPES}` | 来源类型回答，以逗号分隔。 |
| `{EDITOR}` | 编辑器回答。 |
| `{DATE}` | `YYYY-MM-DD` 格式的当前日期。 |

从 `references/templates/domain-page-types.md` 注入页面类型片段：

| 领域 | 添加的页面类型 |
| --- | --- |
| 书籍／媒体 | 角色、时间线、情节线、主题、地点。 |
| 研究主题 | 论文摘要、主张、方法、数据集。 |
| 个人 | 日志条目、目标、习惯、经验。 |
| 企业／团队 | 决策日志、会议摘要、项目、利益相关者。 |
| 其他 | 除非用户提供了更明确的分类法，否则使用通用页面类型。 |

如果编辑器是 Obsidian，向 `SCHEMA.md` 追加 `## Obsidian Setup` 小节：

- 将附件文件夹路径设置为 `raw/assets/`。
- 推荐插件：Dataview；需要制作幻灯片时使用 Marp。
- 使用关系图视图检查 wiki 结构。
- 如果使用 Web Clipper，为下载附件绑定快捷键。

不要把编辑器专用设置放入指针文件。

## 阶段 4：生成指针文件

对于所选的每个非“其他／通用”运行时，使用 `references/templates/agent-pointer.md` 创建精简指针。

| 运行时 | 路径 | `{SCHEMA_PATH}` |
| --- | --- | --- |
| Claude Code | `{wiki-root}/CLAUDE.md` | `./SCHEMA.md` |
| OpenAI Codex | `{wiki-root}/AGENTS.md` | `./SCHEMA.md` |
| Copilot（VS Code） | `{wiki-root}/.github/copilot-instructions.md` | `../SCHEMA.md` |

指针文件仅包含身份上下文、指向 `SCHEMA.md` 的重定向和最少量有用的触发提示。

## 阶段 5：生成初始 Wiki 文件

创建以下种子页面：

| 文件 | 模板 | 自定义内容 |
| --- | --- | --- |
| `wiki/index.md` | `references/templates/index.md` | 添加通用小节和领域专用小节。 |
| `wiki/concept-table.md` | `references/templates/concept-table.md` | 用当前日期填充 `{DATE}`；概念行保持为空。 |
| `wiki/log.md` | `references/templates/log.md` | 添加带当前日期的第一条 wiki 创建记录。 |
| `wiki/overview.md` | `references/templates/overview.md` | 添加简短占位内容，说明 wiki 的目的和领域。 |

通用索引小节：核心地图、来源、实体、概念、比较、综合。

领域专用索引小节：

| 领域 | 小节 |
| --- | --- |
| 研究主题 | 论文、主张、方法、数据集。 |
| 书籍／媒体 | 角色、时间线、主题、地点。 |
| 个人 | 日志、目标、习惯、经验。 |
| 企业／团队 | 决策日志、会议、项目、利益相关者。 |

空白小节使用占位注释，不要虚构内容。

## 阶段 6：编辑器配置

如果编辑器是 VS Code，创建 `{wiki-root}/.vscode/settings.json`：

```json
{
  "files.exclude": { "**/.DS_Store": true },
  "editor.wordWrap": "on",
  "markdown.preview.breaks": true
}
```

如果编辑器是 Obsidian 或其他／纯文件，除了已经追加到 `SCHEMA.md` 的 Obsidian 指南外，不要创建编辑器设置。

## 阶段 7：总结

创建完所有文件后，报告：

```text
已在 {wiki-root}/ 创建 Wiki 脚手架

结构：
  raw/          -> 在此放置来源文档
  wiki/         -> 由 LLM 维护的页面
  wiki/concept-table.md -> 持续维护的概念地图
  SCHEMA.md     -> 智能体行为的唯一事实来源

指针文件：
  {列出生成的指针文件；如果没有则填写“无”}

后续步骤：
  1. 使用 {editor} 打开 {wiki-root}/
  2. 将第一个来源添加到 raw/
  3. 告诉智能体：“读取 {wiki-root}/SCHEMA.md，然后提取 raw/{filename}”
```

除非用户明确要求或当前偏好规定必须启用，否则不要在 bootstrap 期间初始化 BM25。如果用户要求 BM25，请在基础脚手架完成后遵循 `references/workflows/bm25.md`。
