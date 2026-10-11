# Repolex Knowledge Graph of jazzband/django-queued-storage

RDF knowledge graph data for [jazzband/django-queued-storage](https://github.com/jazzband/django-queued-storage), parsed by [repolex](https://repolex.ai).

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
rlex download jazzband/django-queued-storage
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1cbb3c973e2dc6b1f4b8823ac3306111581067a5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1cbb3c973e2dc6b1f4b8823ac3306111581067a5
│           └── chunk-001.nq.gz
├── blob
│   ├── 087a8637212c836bb8da118600926a3d041d1b1c.nq.gz
│   ├── 1240872a743307d51c46f8c2ae78a6db97c43be7.nq.gz
│   ├── 1499dbce4661f4c292a15bbcd993a74d1525c38c.nq.gz
│   ├── 1b43df8b67a4203dc73a3bb55067c7fdf2a481ac.nq.gz
│   ├── 291f33ea938acb9a7087cc3ee50d6488f09611db.nq.gz
│   ├── 2c3bafb5a72328694dd90013a3f81292d243c53b.nq.gz
│   ├── 36ee411ec717dc08c29c47ddcf0073ce4525eb26.nq.gz
│   ├── 37e1d4bb0b37bb7e9e7f4619fc1b7b45e6e7f7b2.nq.gz
│   ├── 40bfeb47c7c825d8c71fb7fa15a7217a44c95a93.nq.gz
│   ├── 44accd2fb4cc0210d1f7e918ed0cda0923fc7e0b.nq.gz
│   ├── 45647aa0a0e1c3e0b2235fa945d8c7052a78ff36.nq.gz
│   ├── 52cb80f502b2b854c4d0fabd5635376bf63bbcdd.nq.gz
│   ├── 54f06cfe698d1996c12d270f2001129d01063a37.nq.gz
│   ├── 5de337e216cbd8638b8cb48c255de3337a923bd1.nq.gz
│   ├── 69c8306c6752324f4d57ea2c859bea9da79f7046.nq.gz
│   ├── 6a50c63871878098992a54b94d9dcef4f95a3ee8.nq.gz
│   ├── 7383ac68e7edcc7357804954cfd3fc8fcdadecd0.nq.gz
│   ├── 789e05ff824ba42d9a773131083b77b7b1d817f1.nq.gz
│   ├── 7c4b7200607d1f55b27faf7fa0ffca0930582a06.nq.gz
│   ├── 943da3e9b864d07f211cf7514e83bb6f7748593c.nq.gz
│   ├── 957f2fbc3cbb998aab75c01010b1a67a8eef71ab.nq.gz
│   ├── 97d62aaee29b933133b3ac012ce971eee78c05d7.nq.gz
│   ├── 9aafa8bb094eac5bb483ea6762384d7b46d2eab4.nq.gz
│   ├── a2c8aceb237b7953b00d549b3d31ea56ddf17fa8.nq.gz
│   ├── ab6855c9bf25ce96da6374d73243da3e3beb7f4d.nq.gz
│   ├── b90a4029064bc03aaba98bd90428dc498006fba0.nq.gz
│   ├── bb306464b62ea1ecc8b35c69341246717c9a2596.nq.gz
│   ├── c1431dc07ab770a3e80fde85461e7e738886c725.nq.gz
│   ├── c533407b42b7e056826173985d6561e261aa9fad.nq.gz
│   ├── cc1613dd4c58b85b92204a5a8032ebd6ccea0f4b.nq.gz
│   ├── d5724b4669348d51f3f7345168967c3db3a8c2e9.nq.gz
│   ├── d71ec4c455ef4f3fb5c1b14bb15f23a79dd3b9f9.nq.gz
│   ├── e0d5efab56fb94577e7804603eb6f21f36977cb2.nq.gz
│   ├── e5c0882c2308b2ff7814d933e8d395b600accdfd.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea12074d370ec7bb2adeccb7fcd2f7b596f9d878.nq.gz
│   └── f848fb9bd32449779bca92d4d6ba4768daa7fe62.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1cbb3c973e2dc6b1f4b8823ac3306111581067a5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 45 files
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

[jazzband/django-queued-storage](https://github.com/jazzband/django-queued-storage)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
