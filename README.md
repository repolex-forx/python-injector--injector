# Repolex Knowledge Graph of python-injector/injector

RDF knowledge graph data for [python-injector/injector](https://github.com/python-injector/injector), parsed by [repolex](https://repolex.ai).

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
rlex download python-injector/injector
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5daed12510fafc0bf73b6ef18d2884f78cd5e210
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5daed12510fafc0bf73b6ef18d2884f78cd5e210
│           └── chunk-001.nq.gz
├── blob
│   ├── 03bdca724cd4a475f3b23abcc465c99a652126de.nq.gz
│   ├── 0673a403011ea5d3e20757afe6eb81e61f417477.nq.gz
│   ├── 1be0253892e589bcc0e7c0938351a4129eed5c67.nq.gz
│   ├── 3794d42f00adc69d22865d7226a8a7fc439aa70f.nq.gz
│   ├── 402c47c64ca0840b6bc184fe9ab6c75874668fa2.nq.gz
│   ├── 4c1c065ab38b48ab3e1ef80f325ebd44a934ebaa.nq.gz
│   ├── 50bc8c609f6dddc15e136fa35e07ee781cb74118.nq.gz
│   ├── 63835477e07cc4f9dc6a4d0e44e92cc93f13838e.nq.gz
│   ├── 69b10124cfe8748f217db4ae55dbd0775f1d1833.nq.gz
│   ├── 6e34535360ab46d9a077ed9092c3f1fd93a3fffa.nq.gz
│   ├── 7e97d3ddce9ea583211cb90f94bd68277bdf216d.nq.gz
│   ├── 917f34eab919a8132a9356c0392ae824fbea5048.nq.gz
│   ├── 9f54df52c6aabc7ac35bd06f46ec2f1d03ec16e3.nq.gz
│   ├── a3166fa087f9296f6e6a443ce0a3c97257ef67f6.nq.gz
│   ├── ad91e90cf1a0075a211be4d833bbc503f9d06900.nq.gz
│   ├── beb247d4943c5c090af261b011f6d049f6e9ce09.nq.gz
│   ├── c2d7402ede40ff9c24ffbd20ba176eaa96660666.nq.gz
│   ├── c5cca337c062fad25866b995b22d089e8ceab834.nq.gz
│   ├── ce3037d9e08479786bfcd1f04474b7522318cee1.nq.gz
│   ├── cf7ece3881d2a07f017c14fc6cd1fc186b1e8877.nq.gz
│   ├── d6c5f48c7917bae3cd89fd14a28922e380380820.nq.gz
│   ├── d7dfff461275129b079dbcb15c90cfbafe5e04f2.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec014c944046c7ab9168fa23b17855b7aeb1b5dc.nq.gz
│   ├── ecd46a8dd67e529fbb9e1416e28f1c4aa892e56f.nq.gz
│   ├── f7f1c18f079687f3c4efd5bb369c8cf0ca810112.nq.gz
│   ├── f83503c84974593b287132e795f39afcf09060e2.nq.gz
│   ├── fbe3651a8b27b3f8f8ac64e71fc46c376a373af8.nq.gz
│   ├── fd72bb8dec46da7f17b9b4f118ed434526414848.nq.gz
│   └── ff0d18fc6bc49837df3662a9a4ab43ea4fe1120f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5daed12510fafc0bf73b6ef18d2884f78cd5e210.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 38 files
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

[python-injector/injector](https://github.com/python-injector/injector)

---
*Parsed on 2026-10-17 by [repolex](https://repolex.ai)*
