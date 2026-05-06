# BM25 Search Layer

This directory contains the local BM25 full-text search index for the wiki.

BM25 is optional. It helps the LLM find relevant Markdown passages once the
wiki grows beyond what `wiki/index.md` and `rg` can comfortably cover.

## What BM25 Adds

- Fast local keyword search over wiki pages
- Better recall for names, products, terms, paper titles, APIs, and exact phrases
- A rebuildable navigation layer for query, ingest, and lint workflows
- Exportable chunks for audit, migration, or debugging

## What BM25 Does Not Do

- It does not replace `wiki/` as the knowledge layer.
- It does not replace `SCHEMA.md` as the operating contract.
- It does not judge whether a claim is true.
- It does not understand synonyms as well as embeddings.
- It does not produce final answers. The LLM must read the returned wiki pages
  and synthesize an answer with normal wiki citations.

## LLM and BM25 Cooperation

```text
User question
  -> LLM extracts terms, entities, and intent
  -> BM25 returns candidate chunks
  -> LLM opens the matching wiki pages
  -> LLM reads full context and follows wikilinks
  -> LLM answers with citations to wiki pages
```

BM25 is a retrieval helper. The wiki remains the source of truth.

## Commands

Run commands from the wiki root:

```bash
python3 scripts/wiki_fts.py doctor
python3 scripts/wiki_fts.py build
python3 scripts/wiki_fts.py rebuild
python3 scripts/wiki_fts.py search "query text" --limit 10
python3 scripts/wiki_fts.py stats
```

Export the full indexed corpus:

```bash
python3 scripts/wiki_fts.py export --format jsonl --out exports/bm25-chunks.jsonl
python3 scripts/wiki_fts.py export --format csv --out exports/bm25-chunks.csv
python3 scripts/wiki_fts.py export --format markdown --out exports/bm25-report.md
```

The export contains chunks, metadata, and text. BM25 scores are not exported
because BM25 scores are computed at query time.

## Git Policy

Commit:

- `scripts/wiki_fts.py`
- `indexes/README.md`
- `.llm-wiki-bootstrap/EXTEND.md` if the preferences are project-specific

Usually do not commit:

- `indexes/fts.sqlite`
- `exports/*.jsonl`
- `exports/*.csv`
- `exports/*.md`

The database and exports are rebuildable from `wiki/`.

## Privacy

`fts.sqlite` and exported files contain searchable text from the wiki. If the
wiki contains private notes, customer material, personal journals, or sensitive
research, do not share these files casually.

## Troubleshooting

If `doctor` fails, the local SQLite build does not include FTS5. Use a Python
distribution with SQLite FTS5 enabled, or continue with `index.md + rg`.

If `stats` says `Fresh: no`, rebuild:

```bash
python3 scripts/wiki_fts.py rebuild
```

If search returns nothing, try exact terms from the wiki, product names, paper
titles, or run `rg` as a fallback.
