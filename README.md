# Repolex Knowledge Graph of modal-labs/vprox

RDF knowledge graph data for [modal-labs/vprox](https://github.com/modal-labs/vprox), parsed by [repolex](https://repolex.ai).

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
rlex download modal-labs/vprox
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4d5a397cf1a5bbc54f33f47589d3de396ec64be3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4d5a397cf1a5bbc54f33f47589d3de396ec64be3
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f107152cf5fad861b5d3935e9308ccfc984108a.nq.gz
│   ├── 1b9a11bd04c856476e132e2b45efcca2effa89ea.nq.gz
│   ├── 237883a5ffca1b893394367222be693bf580152e.nq.gz
│   ├── 3922f81e0a048263609b5a71a7434d8b1156bca0.nq.gz
│   ├── 398e621d2c5b97a72477ad4a96933742397981f3.nq.gz
│   ├── 3d0d184f9525877386e24349123fff7532dbc427.nq.gz
│   ├── 3d28b21b70049b7cb8e93f3a201bf2af7cc2c6a5.nq.gz
│   ├── 436201cf8df777a7b9efae17e6814c0d8b36b713.nq.gz
│   ├── 4639c905db066631de58f7bd67b839ab9331ee89.nq.gz
│   ├── 4854ed9e416f4d56bc78e726cda7778b91fd4eab.nq.gz
│   ├── 4caf5b7d3cd265398e6ce8670bc31c21c93ce6b8.nq.gz
│   ├── 515cd5068f9a3a689a3c93f2719e367daf8a66cb.nq.gz
│   ├── 5696a40ea4a360c9fffefb214dc826d2a92d4247.nq.gz
│   ├── 5b488776f1294cc375da6ebd847a18db41f58ff5.nq.gz
│   ├── 7a55be89cb21e5b08b1b1a1701964e791d66c801.nq.gz
│   ├── 7afa9ba41cad688699164c40661f79c20fe493ce.nq.gz
│   ├── 88f064c70f0be3c532b21cf208a1dc4c87c2e227.nq.gz
│   ├── 8b4f101dd8dbc2776e7a0f892985d808b4a0175e.nq.gz
│   ├── 8fa035573ef2e139f4660f842ca8fc6e180aad5d.nq.gz
│   ├── a7d72d65e9bc1e10b084e3b5967ef0f4cfed2b03.nq.gz
│   ├── ae5fec3e943e53918d715b13e0fddfc47a4033bd.nq.gz
│   ├── afca07b74c3b844da83e637488572a31aeb06cc8.nq.gz
│   ├── cd2ef621177db4f5a9f7c51827cae3913bb55079.nq.gz
│   ├── d20a0a71f33c0d749bc50af69dae57f34cd59a40.nq.gz
│   ├── e693e4dda61298f7748babfb12d7837096bb1a16.nq.gz
│   ├── f024298d2bce40b7ecea541dc8947723eca13ef0.nq.gz
│   └── fc4ee4004bed0c463d7991c8777a3e7f0f8d29fd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4d5a397cf1a5bbc54f33f47589d3de396ec64be3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[modal-labs/vprox](https://github.com/modal-labs/vprox)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
