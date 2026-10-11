# Repolex Knowledge Graph of aio-libs/aioelasticsearch

RDF knowledge graph data for [aio-libs/aioelasticsearch](https://github.com/aio-libs/aioelasticsearch), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aioelasticsearch
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 81b6ae343489cefe84b1d77f758315e6d0bff3c2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 81b6ae343489cefe84b1d77f758315e6d0bff3c2
│           └── chunk-001.nq.gz
├── blob
│   ├── 0284d00cd44a6523492efd00d9733f80136a5483.nq.gz
│   ├── 06ec12548b134d8a25ac81e32503acf872ccd02d.nq.gz
│   ├── 1e3893ae01883d0bb30cc8eccbbee8ab0bbdba23.nq.gz
│   ├── 232f5269405c2ab5156c245b66d34bf5f366f75e.nq.gz
│   ├── 321c757569ad34350c9497af68a946fda51cbd61.nq.gz
│   ├── 38b3a78cc7bb4e7fed204849d59dd4029f0e7fec.nq.gz
│   ├── 44f7e27116eb850b1eaeba0f0381c6bae421ac68.nq.gz
│   ├── 472d66b7cf8f94d17f477e7a343cb9aba693e07a.nq.gz
│   ├── 4de2098f0fad1cb46ea4e6387d3b90b862259162.nq.gz
│   ├── 510d0a90bbe1d1d4fa0e55bfc18d00f415858532.nq.gz
│   ├── 570ba28061a3878c7e7d8475160fb41e83eae4db.nq.gz
│   ├── 59d1c3a7f04239be337869a91a42e7eadb253cbe.nq.gz
│   ├── 6ea20650afd318e6f414b05025314b348b228afc.nq.gz
│   ├── 6ffcf2d2b77f641b5f3c241a0492d748d08634a8.nq.gz
│   ├── 84b1fa1b9a4d979dee785354836c06b02ef95339.nq.gz
│   ├── 85ebeddeeaeae20a4497665a68472ca07db30ed0.nq.gz
│   ├── 8fe11127fa25bbd8c6129538ee685e0b7a0f9747.nq.gz
│   ├── 9733f96ee97e544f7f2f38e15655dc06913057bd.nq.gz
│   ├── a4e19e5eec3f7b79df4e0588ea8c44c6736c05d1.nq.gz
│   ├── c15645289339abc2163f177ba220fc3675344742.nq.gz
│   ├── ca2f33b308e8f84bb805fdb87142c280b3f0ef29.nq.gz
│   ├── ca96238d1360c886443371d66c474d5f75894489.nq.gz
│   ├── d6099c828fc7cba64616004742fceb990d663e34.nq.gz
│   └── e24206f7951ce600070c653a55f024bdf4d78a08.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 81b6ae343489cefe84b1d77f758315e6d0bff3c2.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[aio-libs/aioelasticsearch](https://github.com/aio-libs/aioelasticsearch)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
