# Repolex Knowledge Graph of google-deepmind/videoprism

RDF knowledge graph data for [google-deepmind/videoprism](https://github.com/google-deepmind/videoprism), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/videoprism
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4f831e332b80d6e77bdd43882206f23aba2a67a7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4f831e332b80d6e77bdd43882206f23aba2a67a7
│           └── chunk-001.nq.gz
├── blob
│   ├── 102f68d1604152dac9ccdff2e0253ccf4bae6d64.nq.gz
│   ├── 167e03f0b80cb33b5aecc67011c81ce444516af3.nq.gz
│   ├── 19f131c2f6bb7b0c062adb69a2a00828fb89f552.nq.gz
│   ├── 20c1a06db1fa8bc41cf7ffd9edf79862fc3d82e9.nq.gz
│   ├── 26d4f92e983d3b3b31f336b1c84b3f58c74edb48.nq.gz
│   ├── 3095027071b5c8f52aec866f81da7fec4c5222a3.nq.gz
│   ├── 4028a8aeb53ce7cffae369c83e8ddf773eb09be3.nq.gz
│   ├── 439e91a91df4fb1d41645c97ddb3ce7efe984e59.nq.gz
│   ├── 4e985fbe0daa981c85ee6c8ca1da73b89489f57a.nq.gz
│   ├── 4ef93685f160532da9857b1cdd05bbfa52752951.nq.gz
│   ├── 7a4a3ea2424c09fbe48d455aed1eaa94d9124835.nq.gz
│   ├── 7b5cc74d26e703f27a95827316711fce6b2bd4e7.nq.gz
│   ├── aa6167a640e8fb61500329d1e2e7ac5300fffc67.nq.gz
│   ├── bc8a13ee97c932174c26963d6ae579877a06b63e.nq.gz
│   ├── c64def83fbfa1850ce62fb0b04c39886826c571d.nq.gz
│   ├── cbd79006eb22b244e1bd2d45a4da5df689431a13.nq.gz
│   ├── d5fd4f5732d29a630cf429683a6c203ad0dfad26.nq.gz
│   ├── e05c422b7d0e86678fb4b06a807811467dd57b4f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f29b8dccc7e402bdd597f317eb1947fcae7f697d.nq.gz
│   └── f756e2e6a585cd0af379648f0bcc85bbb2370d1c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4f831e332b80d6e77bdd43882206f23aba2a67a7.nq.gz
├── issue
│   └── issue.nq.gz
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

[google-deepmind/videoprism](https://github.com/google-deepmind/videoprism)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
