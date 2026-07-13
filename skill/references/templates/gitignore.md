# LLM Wiki 的 .gitignore 模板

# 操作系统文件
.DS_Store
Thumbs.db

# 编辑器元数据（Obsidian 会创建自己的元数据）
.obsidian/workspace.json
.obsidian/workspace-mobile.json

# 临时文件
*.tmp
*~

# Python 字节码和本地工具缓存
__pycache__/
*.py[cod]
.pytest_cache/
.mypy_cache/
.ruff_cache/

# 可重建的本地 BM25 产物
indexes/fts.sqlite
exports/*.jsonl
exports/*.csv
exports/*.md
