# Repolex Knowledge Graph of plotly/dash-ag-grid-AI-example

RDF knowledge graph data for [plotly/dash-ag-grid-AI-example](https://github.com/plotly/dash-ag-grid-AI-example), parsed by [repolex](https://repolex.ai).

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
rlex download plotly/dash-ag-grid-AI-example
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3e16de68121e34f58ffae3b913fad0fb06793b02
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3e16de68121e34f58ffae3b913fad0fb06793b02
│           └── chunk-001.nq.gz
├── blob
│   ├── 1aa071ffda8cbade8f3a2d5526e963164d0e85c8.nq.gz
│   ├── 4ae0d6c785c29ae29a8adb72526805506e6f2b1b.nq.gz
│   └── 808a9a0934abc3a1518c172fd68cbdde51717d15.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3e16de68121e34f58ffae3b913fad0fb06793b02.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 9 files
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

[plotly/dash-ag-grid-AI-example](https://github.com/plotly/dash-ag-grid-AI-example)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
