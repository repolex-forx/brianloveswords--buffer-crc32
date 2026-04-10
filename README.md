# Repolex Knowledge Graph of brianloveswords/buffer-crc32

RDF knowledge graph data for [brianloveswords/buffer-crc32](https://github.com/brianloveswords/buffer-crc32), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download brianloveswords/buffer-crc32
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e9b66c7356f4ea6f7c2f89d51160a1ef6117849f
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── e9b66c7356f4ea6f7c2f89d51160a1ef6117849f.nq.gz
│   └── repolex
│       └── e9b66c7356f4ea6f7c2f89d51160a1ef6117849f
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d9d8b83595b57dd04076fd2372ac47b4e526750.nq.gz
│   ├── 221214933cdb6e59ba34df3b634eb822528f438f.nq.gz
│   ├── 4cef10eb7b161e48e39d2cc4def3fd81db6cf884.nq.gz
│   ├── 6727dd39bb09ada1f02f48e11cacb435b86771c7.nq.gz
│   ├── b512c09d476623ff4bf8d0d63c29b784925dbdf8.nq.gz
│   ├── b6b68f4ae3d83fa1c7c34d185e855b23847decc0.nq.gz
│   └── e896bec584f960a953beb3b1f2291f5e33439a86.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── e9b66c7356f4ea6f7c2f89d51160a1ef6117849f.nq.gz
├── filetree
│   └── e9b66c7356f4ea6f7c2f89d51160a1ef6117849f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 17 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |

## Source repository

[brianloveswords/buffer-crc32](https://github.com/brianloveswords/buffer-crc32)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
