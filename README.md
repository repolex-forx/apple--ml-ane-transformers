# Repolex Knowledge Graph of apple/ml-ane-transformers

RDF knowledge graph data for [apple/ml-ane-transformers](https://github.com/apple/ml-ane-transformers), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download apple/ml-ane-transformers
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── da64000fa56cc85b0859bc17cb16a3d753b8304a
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── da64000fa56cc85b0859bc17cb16a3d753b8304a.nq.gz
│   └── repolex
│       └── da64000fa56cc85b0859bc17cb16a3d753b8304a
│           └── chunk-001.nq.gz
├── blob
│   ├── 07333003bfc528436b9365476269c6073e2a2674.nq.gz
│   ├── 12d06bfcfdb71cc29bd953e6c370990988b1e022.nq.gz
│   ├── 24688d48b9773ad153c8b30e739e9211ec3206f7.nq.gz
│   ├── 30438b7acc04fd4f48ca4a5423f2b35d559b037b.nq.gz
│   ├── 44843fb6d77e675ec9cdfac2bc78796960af85c3.nq.gz
│   ├── 4845c22e3e01207cb451a61daeb9790fc46356bc.nq.gz
│   ├── 5d659ae410c78391c3134e7bff5d2815a6e930fc.nq.gz
│   ├── 649894210de673468e94891b2a866537b95de6ea.nq.gz
│   ├── 766ec5290509a7803136db014515f42d3780fad2.nq.gz
│   ├── 7971439226fd6a5a708c53aee54957b04aa3dfae.nq.gz
│   ├── 7aa670ac23e18aefef52c437029dd5540d5a1d09.nq.gz
│   ├── a3241484e68c20b7aa3aefcc445477b4c75062d7.nq.gz
│   ├── a59eeb0ec72dc732c65afe4369231731df90f19e.nq.gz
│   ├── aea4595aa8f952126690b58cb81df9ec12c52b03.nq.gz
│   ├── b14f14d3025f22f11973fc817642d8c811795cac.nq.gz
│   ├── b6f55df7741c38d68f8dc591d2378dfa7cb5b0a5.nq.gz
│   ├── bdd8059fd57e0ddb95375735b8fd8fb6627aa11b.nq.gz
│   ├── c13e927915b01ebcc567e02fac5e869bbda67284.nq.gz
│   ├── c280260c117371ee94b830eb698bc33ddb57dcc5.nq.gz
│   ├── c991377a60951acbcd7f586ebcf0184840e30e55.nq.gz
│   ├── d70da744e9813cfcaa2a93d5f201a3f8d8600de5.nq.gz
│   ├── dad2ff5db843081dabd3a7f3a007c8bbdcd036f8.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e8bf3ac0b68e8a0980554243e5addd8c49d5db2c.nq.gz
│   └── ef9cf18f2024e66e0377ca842008034dd30c6076.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── da64000fa56cc85b0859bc17cb16a3d753b8304a.nq.gz
├── filetree
│   └── da64000fa56cc85b0859bc17cb16a3d753b8304a.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 34 files
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

## Source repository

[apple/ml-ane-transformers](https://github.com/apple/ml-ane-transformers)

---
*Parsed on 2026-04-22 by [repolex](https://repolex.ai)*
