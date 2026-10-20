# Repolex Knowledge Graph of klen/http-router

RDF knowledge graph data for [klen/http-router](https://github.com/klen/http-router), parsed by [repolex](https://repolex.ai).

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
rlex download klen/http-router
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ab775319ef7933391cf9ff524bb9b105e1fc47be
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ab775319ef7933391cf9ff524bb9b105e1fc47be
│           └── chunk-001.nq.gz
├── blob
│   ├── 092f845b8be360abeccb316f26b0c4faec1da366.nq.gz
│   ├── 24ee5b1be9961e38a503c8e764b7385dbb6ba124.nq.gz
│   ├── 252a34be779f7b397352699bfe86213c4367943c.nq.gz
│   ├── 26a35962098d30ca38de58b2c09648c6bf92790f.nq.gz
│   ├── 29d1b1a71115311984b0cfc4f5d71fd5b50a15f9.nq.gz
│   ├── 2e188149de63057d84c36fd6608677d46aac49cc.nq.gz
│   ├── 3fedd75b66b77ae97911f4a5b1403d49dfb9c625.nq.gz
│   ├── 4327228172aa73916b8028d2594f32ef3e687f69.nq.gz
│   ├── 470f7d528c1994878cfc53bfef115056aebe6e0d.nq.gz
│   ├── 511da94f0c4079bbd15e073583e65e7138740992.nq.gz
│   ├── 51f0c212827d10cd1b0d4f0b35a29fc7a247c211.nq.gz
│   ├── 65645224853240d4fddec268fa791f2e2c30cb41.nq.gz
│   ├── 6ac5b1916b27700dbfb6967c5bc9d3cde611d051.nq.gz
│   ├── 6b33cce13bf9e015fc8274ea09554174ed9a29a4.nq.gz
│   ├── 6bc192aa81fe86b153dbe40677a57de244231da2.nq.gz
│   ├── 72acc135bba913f9dcf6bafada17e997738a5ec1.nq.gz
│   ├── 86d16b1da73508d9b49ef7d64d3ec8ab7809e740.nq.gz
│   ├── 89a0c38e826334e137bd83b6d4c4564656d4beb0.nq.gz
│   ├── 8f74a08d8e8ce25d2169fb13624ed0944ad3ab56.nq.gz
│   ├── a54697a53602e47217bd4e24309aa32a357d76c0.nq.gz
│   ├── b562f73df3c4fb04601c8506194df8fa5f2ba014.nq.gz
│   ├── b672ef47541f92fca95c569564d9e1e063f27fd6.nq.gz
│   ├── c0873f9d2b9e6aaaed3fbdca4e124b3e210e31a7.nq.gz
│   ├── c9614892d464737c8f95ec122805f980f208d436.nq.gz
│   ├── ca2d71b338141dadf4f38288678256ee36815f4d.nq.gz
│   ├── cca61a2f09736618e5b1ba1f8172242469ffb5f1.nq.gz
│   ├── d4744759a41b1fe43faa2f7ef3d51a371b5deb61.nq.gz
│   ├── d96254bcc278823d392015b1067576b9a97c799a.nq.gz
│   ├── e349922130a43b4f78cd5e408ecc493750a7ce88.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── eb3c4b8b39572207afb7f057a1ca7befb627e0df.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ab775319ef7933391cf9ff524bb9b105e1fc47be.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[klen/http-router](https://github.com/klen/http-router)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
