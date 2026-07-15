# Log

> Append-only chronological record of all wiki operations.
> Each entry: `## [YYYY-MM-DD] operation | subject`
> Parse with: `grep "^## \[" wiki/log.md | tail -10`

## [2026-05-06] init | Wiki Rebuilt

- Scaffolded by llm-wiki-bootstrap from `karpathy-llm-wiki-original.md`
- Domain: LLM-maintained persistent Markdown knowledge bases
- Source types: Markdown article
- Schema: SCHEMA.md (single source of truth)
- Pointers: AGENTS.md

## [2026-05-06] ingest | LLM Wiki

- Summary: wiki/sources/karpathy-llm-wiki-original.md
- Updated: wiki/overview.md, wiki/index.md, wiki/concept-table.md
- New pages: wiki/concepts/filed-query-artifacts.md, wiki/concepts/human-curation-loop.md, wiki/concepts/index-and-log-navigation.md, wiki/concepts/llm-owned-wiki-maintenance.md, wiki/concepts/llm-wiki.md, wiki/concepts/local-search-layer.md, wiki/concepts/persistent-compounding-artifact.md, wiki/concepts/rag.md, wiki/concepts/schema-as-operating-contract.md, wiki/concepts/source-of-truth-separation.md, wiki/concepts/wiki-operations-loop.md, wiki/entities/claude-code.md, wiki/entities/dataview.md, wiki/entities/marp.md, wiki/entities/memex.md, wiki/entities/notebooklm.md, wiki/entities/obsidian.md, wiki/entities/openai-codex.md, wiki/entities/qmd.md, wiki/comparisons/index-navigation-vs-search-layer.md, wiki/comparisons/rag-vs-llm-wiki.md, wiki/synthesis/how-to-operationalize-llm-wiki.md, wiki/synthesis/why-llm-wikis-work.md
- Contradictions: none

## [2026-05-06] bm25-init | Search Layer Enabled

- Preferences: llm-wiki/.llm-wiki-bootstrap/EXTEND.md with bm25.mode required
- Database: indexes/fts.sqlite
- Script: scripts/wiki_fts.py
- Pages indexed: 28
- Chunks indexed: 115
- Export: exports/bm25-chunks.jsonl

## [2026-07-15] ingest | TOGAF 标准——架构开发方法

- Summary: wiki/sources/c220-part1e-architecture-development-method(TOGAF 标准——架构开发方法).md
- Updated: wiki/overview.md, wiki/index.md, wiki/concept-table.md
- New pages: 16 concept pages, 2 entity pages, 1 source-summary page
- Source: C220-Part1e-Architecture Development Method.md
- Language: Chinese compilation requested by user
- Contradictions: none identified
- BM25 preflight: initialized with the bundled Python 3.12 runtime after the `python3` launcher failed; 47 pages and 142 chunks indexed after ingest

## [2026-07-15] rename | TOGAF 页面双名文件迁移

- Scope: 本次 TOGAF 摄取产生的 19 个来源、概念和实体页面
- Format: `english-slug(中文标题).md`
- Updated: wiki/index.md, wiki/concept-table.md, wiki/overview.md, wiki/log.md and all affected internal links
- Excluded: 既有 LLM Wiki 页面与 raw/ 原始资料
