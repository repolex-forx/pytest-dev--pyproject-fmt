# Repolex Knowledge Graph of pytest-dev/pyproject-fmt

RDF knowledge graph data for [pytest-dev/pyproject-fmt](https://github.com/pytest-dev/pyproject-fmt), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pyproject-fmt
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 248a2541c72e456619338e1bd372242e08d64fd2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 248a2541c72e456619338e1bd372242e08d64fd2
│           └── chunk-001.nq.gz
├── blob
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 364982344fbd94d55705e1f27a9a87abaa255333.nq.gz
│   ├── 43c85e79255e2b09a3c021d3b1bf357e3c6676ba.nq.gz
│   ├── 4425c229252139bd2641fda4badd61ca3cf27f6c.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 665ae512db05e06307dfe50832929d53a908a76d.nq.gz
│   ├── 6672d106fecd2c5fb42c492c6c1c761589a81a02.nq.gz
│   ├── 75b94899d666ab2d3cfeb69e95c2114765b443d1.nq.gz
│   ├── ab527f0acf7ebd3ce108ad5e8acfdbf4355d0b06.nq.gz
│   ├── acd071cc82d5d6620ef7caedb1bc2fc7eb89f2a2.nq.gz
│   ├── ae419c100b25005bd082785a7709b42a9e0300ba.nq.gz
│   ├── be0cb7952afbec927c8a6ad4fe1815786a5fc9a0.nq.gz
│   ├── cbc2f0858ab7fb15e68268ac3bd7bfb223efa1d2.nq.gz
│   └── f519bca90c5ef8b0f2d9c8de96ca02778df0a662.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 248a2541c72e456619338e1bd372242e08d64fd2.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 20 files
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

[pytest-dev/pyproject-fmt](https://github.com/pytest-dev/pyproject-fmt)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
