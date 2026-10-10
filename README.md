# Repolex Knowledge Graph of samuelcolvin/pytest-pretty

RDF knowledge graph data for [samuelcolvin/pytest-pretty](https://github.com/samuelcolvin/pytest-pretty), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download samuelcolvin/pytest-pretty
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6233b5ab95308a1dba68198492c2705efe387ede
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6233b5ab95308a1dba68198492c2705efe387ede
│           └── chunk-001.nq.gz
├── blob
│   ├── 33f73dcbe1e49f7498ed6506915941c93e818e70.nq.gz
│   ├── 3587e90e827ed041a7e990523a5ed2ab9e5660af.nq.gz
│   ├── 47de40dc06ba673d480a12ef728ce62fe43e3151.nq.gz
│   ├── 4e6405832874d9509a0c2c226c2fe2b9c9c0c55c.nq.gz
│   ├── 52eb11cb4d6f0279936282ac8018e2c7d8fea982.nq.gz
│   ├── 570f6f79b423ecf5d53c2bf581ade93e1f8bec9a.nq.gz
│   ├── 597bc0eedab645a799a1ef3bff5822ae2d434de8.nq.gz
│   ├── 7e4248fab6d84f3a1da1b3ff07937275bb78b858.nq.gz
│   ├── 8cc5ad8eeff6908033122e5f9daaeb5ca1de4932.nq.gz
│   ├── ac973c96a96d631f00cb9278b81850aa359029cf.nq.gz
│   ├── cdd6d45a4f704d3d1b3e3ed0d3f23d451c839bc4.nq.gz
│   ├── db4683a1560f6893b552c687622b0f734941a834.nq.gz
│   └── ed5d36479cf4c88e1f4ca896d0989e68a297cb43.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6233b5ab95308a1dba68198492c2705efe387ede.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[samuelcolvin/pytest-pretty](https://github.com/samuelcolvin/pytest-pretty)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
