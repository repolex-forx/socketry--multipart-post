# Repolex Knowledge Graph of socketry/multipart-post

RDF knowledge graph data for [socketry/multipart-post](https://github.com/socketry/multipart-post), parsed by [repolex](https://repolex.ai).

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
rlex download socketry/multipart-post
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cce3634876b74e08a6c51d02db00070a82dc8cc4
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cce3634876b74e08a6c51d02db00070a82dc8cc4
│           └── chunk-001.nq.gz
├── blob
│   ├── 059143ac013821ca1858cd28b904a7cf6df7f933.nq.gz
│   ├── 09a72e068cf9760364dae84cdf212fa51dcd96d1.nq.gz
│   ├── 0c4d915fd3468477422444fbc4b1f057a3261eaa.nq.gz
│   ├── 16f8f4b7019bd875c97e1c369a260030a95d46b3.nq.gz
│   ├── 181374dfee89034d32ee4f6206e5166c5602eb8a.nq.gz
│   ├── 21898f54e4a7b5db84c4980bc263e3c0adb3ab8e.nq.gz
│   ├── 24a84b0457db99f7424cc94bb05ed4bd52a84147.nq.gz
│   ├── 3b080f3c9e7277d75b8f8d107b4a4e1164e787a6.nq.gz
│   ├── 41296c2f422e2523c921f73e833c4d0374bde6e7.nq.gz
│   ├── 4f22b3d998d7bb28e0b146515189316ce2d0a15b.nq.gz
│   ├── 5fa1a8ddfb226552b39f6d8eff1c25f12194b561.nq.gz
│   ├── 68adbf24628f002e0ee33274eae24f0226e521f5.nq.gz
│   ├── 70672bd43e4f7dea8d57e6a0636897b2c7342080.nq.gz
│   ├── 84d22c88b6e76f28900b6f863066fc62cd008176.nq.gz
│   ├── 89f40fef4a7abdec2ee1e624ca9e7881e0505ac3.nq.gz
│   ├── 8f76f57839bf00eeb1fb80d503cd575ebc1dd22c.nq.gz
│   ├── 94c986d78915c9b2b69ff522165f61ff9331418f.nq.gz
│   ├── 973f5b982951124eda8247113581a6018a8b9149.nq.gz
│   ├── a6e7d262430919a9468c27ef7f42e55a3eeba67d.nq.gz
│   ├── af2ffcdcfac3a4242cd9e2ef9c576aeda312d21e.nq.gz
│   ├── b7deff8a994bbc0e8e18ecfe14c9de9393d4e36f.nq.gz
│   ├── bcbaebc887135d8d9e9e7dee651e4af4f4db6f88.nq.gz
│   ├── c16a0e64fdca564c1eec61f94f3e1e69d0187482.nq.gz
│   ├── cfafe795021b3b04d832ec7de25b917260b87fef.nq.gz
│   ├── d179b82d505aa978a64a843b3a703a843a718c5e.nq.gz
│   ├── d77c0dbe8694c7d5206447e2ca1e8cf2488fa647.nq.gz
│   ├── d98e595fc6f3b8b88f2d1b49c1ddec4bbefbb896.nq.gz
│   ├── dc6470c7674f744f617a49ac03f18515571bb51e.nq.gz
│   ├── e5dcaaca303d2e3d91b97cf9b39d4de6750dbadd.nq.gz
│   ├── e670a9f7b2d2e17a8e94f111242821018cf3a2cf.nq.gz
│   ├── f5f553a09b617be9250124ac78bce39295c399d9.nq.gz
│   └── f9c1d599ec6bf6dd43c0159f0f8347a28f6f0c37.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cce3634876b74e08a6c51d02db00070a82dc8cc4.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[socketry/multipart-post](https://github.com/socketry/multipart-post)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
