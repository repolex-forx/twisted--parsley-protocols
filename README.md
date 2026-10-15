# Repolex Knowledge Graph of twisted/parsley-protocols

RDF knowledge graph data for [twisted/parsley-protocols](https://github.com/twisted/parsley-protocols), parsed by [repolex](https://repolex.ai).

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
rlex download twisted/parsley-protocols
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7c56638e7a06b1353cc139e83a9871a8cc412ef0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7c56638e7a06b1353cc139e83a9871a8cc412ef0
│           └── chunk-001.nq.gz
├── blob
│   ├── 0254e15279b136889c106b618518375154550559.nq.gz
│   ├── 02bfa2ce8ceabca6e731e40b5fa137f0763b980f.nq.gz
│   ├── 064524a5429294d4e060d2a8bfd47a1cf0a53f29.nq.gz
│   ├── 1989e55b010323ffa7c035e00cdd7c435d073ce6.nq.gz
│   ├── 1c8f2f379ed634ec2d7b581b65890d7d81c76b32.nq.gz
│   ├── 31d7e529694f3f1bb3ac1571cb0c9089328b5a3f.nq.gz
│   ├── 37fe47deb836403409bc53936cc454402d37bdb6.nq.gz
│   ├── 47ad51bf76075798e4240699037fad39781a44a5.nq.gz
│   ├── 5996c9de1aef767e8e965fe5666b70c020ef4da6.nq.gz
│   ├── 5e29423133ee8c4fdbce42903f386801a62ba7e2.nq.gz
│   ├── 62c3dc0cc2c01868db2e4b70c24806872dd738b1.nq.gz
│   ├── 670b2af89460c68cd5b708f0d3bc6d6e9a2f93ef.nq.gz
│   ├── 6c4d275da47757a6f6babba46f0dc4fe87667a5c.nq.gz
│   ├── 74b2a1696d414faac399f9ec3ce88ef28ad2efd6.nq.gz
│   ├── 76a47b63c15d199993205fdb39366b7ce5763038.nq.gz
│   ├── 8162bcf3c3b110061eb1fec989afd021393c9529.nq.gz
│   ├── a804f135cc578f9fd7c7db4dac834eafc40de447.nq.gz
│   ├── a87e2043f11e3b03014469772bbbeb8aff993646.nq.gz
│   ├── aa97a41fb859623e73674b70a1eca953a13e9f31.nq.gz
│   ├── b273f7e2cafb248ee70964b6b1e62a457504acfb.nq.gz
│   ├── bf3f90b5e49ba503b0ef29d141dd32c60adb9d87.nq.gz
│   ├── c62d14ae6aa5fcb36aba47b3914af4f533170309.nq.gz
│   ├── d567919acf7348e453e6326e523219ac3c4f90bf.nq.gz
│   ├── d7d9c0d6bb108510dc65f63ed21f85cd9821d6c2.nq.gz
│   ├── dfbd28b9b3d2fe5808512fe2f9b89a22b8bf6a95.nq.gz
│   ├── e5c3956195bf138974d9d503dd7c1ca8b5094dc8.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e79fc340e47b9e51f3c7f548812a78be871b4316.nq.gz
│   └── ee97ab922a322666ee641fe6a6f98d3c9cefa9bf.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7c56638e7a06b1353cc139e83a9871a8cc412ef0.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 36 files
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

[twisted/parsley-protocols](https://github.com/twisted/parsley-protocols)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
