# Repolex Knowledge Graph of UKPLab/acl2025-modular-sentence-encoders

RDF knowledge graph data for [UKPLab/acl2025-modular-sentence-encoders](https://github.com/UKPLab/acl2025-modular-sentence-encoders), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/acl2025-modular-sentence-encoders
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2c73b307a560ed8a9016546f51af5c930bb2d6a5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2c73b307a560ed8a9016546f51af5c930bb2d6a5
│           └── chunk-001.nq.gz
├── blob
│   ├── 154e041b01f86dee39459c49b3a38f3b3d9f55d5.nq.gz
│   ├── 1769893cdfb12c7b5d68f244495e7eb33636a2c7.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2c94a836477990bbe671507317331bf1d96676b0.nq.gz
│   ├── 37ca31453549eae92eeeed706b360756a2b5d73f.nq.gz
│   ├── 41e5fe4290dd61aecf68686021f120f8c6d346b0.nq.gz
│   ├── 47c18cb19037e44e4aa5d0e745eefe807d633d48.nq.gz
│   ├── 48551be3428a28784dd7e562be2491eb4290a284.nq.gz
│   ├── 5021c151825cc29b0a6816d0fe15a0fbd1275bed.nq.gz
│   ├── 586a02e5136c291ca39331f71e03a5cf97ca38a8.nq.gz
│   ├── 5ec9d0ecfed0177ae455f18bc0750aedf4102b30.nq.gz
│   ├── 667b1c3903b666a06d191761e1e7a7b824c5042c.nq.gz
│   ├── 6686286ac33c7a60744df010f8ff88bdf72080b1.nq.gz
│   ├── 71ab7c65d775fd1b552172f0c1e5b1a3a022c470.nq.gz
│   ├── 7c6008fe201e741596b0e00d60a298cb7b211db7.nq.gz
│   ├── 90bd407662207e47036ec241d0163e6e6df7af11.nq.gz
│   ├── a6c220b418b67a0b78b50ab8c3d738e7b98eea15.nq.gz
│   ├── a831e61c8d4d66bfaa49d7d69b5eb2def1f2d6c2.nq.gz
│   ├── b4116867bbdb34cc9648574370a799980bdb3cc3.nq.gz
│   ├── b72b7adee8e99f6c734702b722b748bc73836733.nq.gz
│   ├── b7c66551ca92ba12add200129bc2f11a0c066e80.nq.gz
│   ├── b812c1e7810de766136e4fc5c20424db9ad2edb8.nq.gz
│   ├── ba6b1146f56cb39ecce9ebb0a692dcbac7955f40.nq.gz
│   ├── bf5ea8dff06136b8d440d08a4fba3dfa6f2059e5.nq.gz
│   ├── d1ee634045bf3d09ea3a5e84082870cff8101a8b.nq.gz
│   ├── dd68173fb328b917132e8c7e531ee479d051188f.nq.gz
│   ├── e7975024a045f054322b9db56cb7dc011b600b39.nq.gz
│   ├── ec927e663b2160872c32c2cd97f4ccdeed761104.nq.gz
│   └── fe3684e14f2963f46ba3013e24eedeb7139ee124.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2c73b307a560ed8a9016546f51af5c930bb2d6a5.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 35 files
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

[UKPLab/acl2025-modular-sentence-encoders](https://github.com/UKPLab/acl2025-modular-sentence-encoders)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
