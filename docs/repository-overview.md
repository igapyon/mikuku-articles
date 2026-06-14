# mikuku-articles repository overview

## Summary

This repository stores Mikuku-authored article materials.

At the time of inspection, the repository mainly contains one Note article package for
June 6, 2026. The article explains external processing behind generative AI agents
through the metaphor of rabbit-shaped fairy helpers.

## Main Article

- Path: `2026/06/20260606/20260606-general-ai-agent-fairies-outline.md`
- Title: `生成AI agent の向こう側には、いろいろな妖精さんがいる`
- Author metadata: `igapyon`
- Writer agent metadata: `みくく`
- Published target: `note`
- Release date: `2026-06-06`
- Published URL: `https://note.com/toshikiigaa/n/ndc1b1eca21fc`

The article is a Japanese technical essay in Mikuku's style. It describes how a
generative AI agent is not doing all work alone. Instead, work is split among the
agent, Agent Skills, MCP, and external or internal processing helpers.

## Article Theme

The article uses three main metaphors:

- `Agent Skills` are described as `魔法書`.
- `MCP` is described as `魔法陣`.
- CLI, API, database access, internal functions, and external services are described
  as `妖精さん`.

The fairy helpers in this article series are specifically presented as rabbit-shaped
helpers. The article classifies them as follows:

| Metaphor | Technical role | Rabbit image |
| --- | --- | --- |
| CLI の妖精さん | Command-line tools and local commands | Bright light-brown Netherland Dwarf |
| API の妖精さん | External service or system API entry points | White and pale-gray Holland Lop |
| データベースの妖精さん | Database and query access | Near-black chocolate Mini Rex |
| MCP server 内部処理の妖精さん | Small processing inside an MCP server | Cream-colored Jersey Wooly |

## Article Sections

The current article contains these major sections:

- `はじめに`
- `妖精さんは、実際に仕事をしてくれる相手`
- `CLI の姿をした妖精さん`
- `API という入口を持った妖精さん`
- `データベースの奥で記録を探す妖精さん`
- `MCP server の中に住む小さな処理の妖精さん`
- `妖精さんは、自分で働くことも、取り次ぐこともある`
- `妖精さんへのお願いには術式がある`
- `妖精さんは万能ではない`
- `魔法書、魔法陣、妖精さん`
- `おわりに`
- `関連する記事`
- `執筆担当`

Additional metadata-oriented sections were also detected in the article file:

- `想定読者`
- `使用ツール`
- `関連リンク`

## Image Assets

Article images are stored under:

- `2026/06/20260606/images/`

The article currently references generated image files from `u000.png` through
`u012.png`. These correspond to the cover image, section images, related articles,
and author credit image.

Shared article images also exist under:

- `2026/images/`

Examples include:

- `byMikuku-3.png`
- `relatedArticles.png`
- `useTools-3.png`

## Image Source Prompts

Image-generation source material is stored under:

- `2026/06/20260606/images/src/`

The cover-level prompt is:

- `2026/06/20260606/images/src/image-prompt.md`

Section-level image source material is stored in numbered directories:

- `2026/06/20260606/images/src/sections/001/`
- `2026/06/20260606/images/src/sections/002/`
- ...
- `2026/06/20260606/images/src/sections/012/`

Each section directory contains:

- `section-text.md`: summary and intent for that section image.
- `image-prompt.md`: image-generation prompt for that section.

## Repository State Notes

At inspection time:

- The Git working tree was clean.
- The repository size was about 87 MB.
- The `2026/06/20260606/images/` directory was about 40 MB.
- `.DS_Store` files were present under image directories:
  - `2026/06/20260606/images/.DS_Store`
  - `2026/06/20260606/images/src/.DS_Store`

The `.DS_Store` files are likely not useful as article source material. They should
usually be ignored or removed from version control if repository hygiene is being
maintained.
