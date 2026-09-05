# Repolex Knowledge Graph of dtolnay/quote

RDF knowledge graph data for [dtolnay/quote](https://github.com/dtolnay/quote), parsed by [repolex](https://repolex.ai).

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
lexq download dtolnay/quote
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 842ffde933fdd76cd1681a288bed136d8b95a97a
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 842ffde933fdd76cd1681a288bed136d8b95a97a.nq.gz
│   └── repolex
│       └── 842ffde933fdd76cd1681a288bed136d8b95a97a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a39f4150704fb168d33408460d00a0a7c8418a1.nq.gz
│   ├── 0e8afe398e8c48f0ce329de4f6e28d7e17c0d9e9.nq.gz
│   ├── 12ad307703657213e3b3fd75980802d4b8b0955c.nq.gz
│   ├── 1ab1fd4a36d6b72b2500fa33429c0871e4562b6b.nq.gz
│   ├── 1b5ec8b78e237b5c3b3d812a7c0a6589d0f7161d.nq.gz
│   ├── 20fe888c30ab44fa877a58de0304f4b5e2a5a5cf.nq.gz
│   ├── 23a6a065ec960a031726c8c26222b0405d4f5851.nq.gz
│   ├── 2553717f905253d5a7cb39b828612f11d3419473.nq.gz
│   ├── 2c740cc0830fd8abd94efc62669e882a66750b89.nq.gz
│   ├── 30adc2d93801c83940ed30d012ef6e8e04a281ea.nq.gz
│   ├── 31aa79387f27e730e33d871925e152e35e428031.nq.gz
│   ├── 46bba332c11728eee831ed81fa2c7e944d03a1d7.nq.gz
│   ├── 50f98cb3bda60408b64c0e88a772486a692f9b07.nq.gz
│   ├── 558997d8fcb480dbd6ae2a7e1c03cc9735391605.nq.gz
│   ├── 62585db9caf0bbaa4054429e3c9e8bb00bc33938.nq.gz
│   ├── 646c9c7d8c9692feecca82135997771bdc506ccf.nq.gz
│   ├── 6afc6b3035597731e3f42a13df1a00647918f134.nq.gz
│   ├── 7044225d1b066387fe465fb4aab47c40ac4c256e.nq.gz
│   ├── 750707701cdae985156601cc906195021ba6a6e5.nq.gz
│   ├── 8908353b57d7388281b27d3a1a85e3143231de39.nq.gz
│   ├── 894d146c5733e5833881885c110c0bf029af8963.nq.gz
│   ├── 9cf199aae2929888ccaff145854ccb2a9a15e8d5.nq.gz
│   ├── a74c68697b422dd8d48f81de565cd40648c78c56.nq.gz
│   ├── a8f0fe773c5d17571ca778e15f444a54e74f8e49.nq.gz
│   ├── ac1426a6c5fdef2770477e9525d8814f93b70529.nq.gz
│   ├── b8eadf5b315a61337e4810d013be8d44cf84d914.nq.gz
│   ├── ba6fe77bc396cf9b54ab70c4eec74c71bee1a1f7.nq.gz
│   ├── bdad175e2a6652becd2aa0cad36678648c31e28a.nq.gz
│   ├── c027243ddac68f75cc3efe86274c65e95548b3c2.nq.gz
│   ├── c3c918ad30d49009197b0279076f448cf577aee9.nq.gz
│   ├── cad5c1daae4cd94573a6093d13376b493e38cc00.nq.gz
│   ├── d48d00de29e9578e68f1972a57df59d474595484.nq.gz
│   ├── d52f255ecca2581b18b3d0e885a582c657df4d9e.nq.gz
│   ├── d5601c8a06f278e91b3decf499c701d6b5e6e857.nq.gz
│   ├── e9e21997b1aca0707f8749ea13c09aec66c899d2.nq.gz
│   ├── ecce96394fc74857fd2709cef49491183667d6df.nq.gz
│   └── f991c1883d6d34de4b28c95ffce6f63ab44d53a2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 842ffde933fdd76cd1681a288bed136d8b95a97a.nq.gz
├── filetree
│   └── 842ffde933fdd76cd1681a288bed136d8b95a97a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 47 files
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

[dtolnay/quote](https://github.com/dtolnay/quote)

---
*Parsed on 2026-09-05 by [repolex](https://repolex.ai)*
