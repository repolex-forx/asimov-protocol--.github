# Repolex Knowledge Graph of asimov-protocol/.github

RDF knowledge graph data for [asimov-protocol/.github](https://github.com/asimov-protocol/.github), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-protocol/.github
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ff7f655a77780c127e2d62b364777bdfd70b5a1c
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── ff7f655a77780c127e2d62b364777bdfd70b5a1c.nq.gz
│   └── repolex
│       └── ff7f655a77780c127e2d62b364777bdfd70b5a1c
│           └── chunk-001.nq.gz
├── blob
│   ├── 03cbe1fed2f6e8f50e54c189e7395e3b199c1d0f.nq.gz
│   ├── 1ce751497fc1ab9ecbf028e9996cc34942191a54.nq.gz
│   ├── 2279ceea5329a0b33be20112019aa726177513ec.nq.gz
│   ├── 2f1fd3e486cca1cb6f7c1b552a46840aa29c5ed0.nq.gz
│   ├── 52bb7b8c9476d64aed499d4bb7c792eac486c599.nq.gz
│   ├── 540553d4875fe96f7658bf793845072f91ee0fca.nq.gz
│   ├── 54c11aebdb5ac033fa2fcb6c91548aae7f9ff1a9.nq.gz
│   ├── 646553e037f1b0ea16966898c0093035cbc17377.nq.gz
│   ├── 7660bdef0ea9f8814e3e8e6b2fd4b87e73c08dd8.nq.gz
│   ├── 8b0bd234485097945177b6c3cbbb5be6de860e52.nq.gz
│   ├── bb67c988519445888ae76a7c7c4041de9dee75cf.nq.gz
│   ├── d9128649efcc068e0569f0d6e80393dac91f978e.nq.gz
│   ├── d9a45be5afa9a98833f7b553903364b0efd74106.nq.gz
│   ├── df2f97f29349e5cb5966703d2f26fde5372e7d86.nq.gz
│   ├── e09d340b6ab9fe039a4e1abdf704a84b012f3beb.nq.gz
│   ├── e1bf5bacf720484e7ac7e8d517f5ad3e03d3e250.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   ├── f38e5018be2f5622b08cea6dd9b259f6e63c4cf2.nq.gz
│   └── f87bec9f1ff19b3bd44bd1c0174260a7cdf6d55c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ff7f655a77780c127e2d62b364777bdfd70b5a1c.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[asimov-protocol/.github](https://github.com/asimov-protocol/.github)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
