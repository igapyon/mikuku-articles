# mikuku-articles

Mikuku-authored Note article packages for GitHub Pages publication.

Articles are organized by year, month, and date under paths such as
`2026/06/20260607/`. Each article package may include the article Markdown,
published-image assets, and image-generation source prompts.

## Agent Skills RAG Draft Preparation

Some draft articles compare how an AI agent searches this repository before and
after adding generated indexes. Those experiments use a local raw clone as the
reference corpus.

After checking out this repository, prepare the raw corpus from the repository
root:

```sh
mkdir -p references/raw
git clone https://github.com/igapyon/mikuku-articles.git references/raw/mikuku-articles
```

If `references/raw/mikuku-articles` already exists, update it instead:

```sh
git -C references/raw/mikuku-articles pull --ff-only
```

`references/raw/` is local working data and is ignored by Git. Do not commit the
raw clone.

## 記事をテーマ別に読む

記事はテーマ別に分類しています。各分類内では、新しい記事からチェックできるように日付の降順で並べています。

### 記事一覧・管理

- 2026-05-31: [note 記事一覧](2026/05/20260531/20260531-note-article-list.md) ([note](https://note.com/toshikiigaa/n/nde411c861a5a))

### トークン消費量

- 2026-05-31: [Agent Skills でトークン消費量を抑える考え方](2026/05/20260531/20260531-token-consumption-03-agent-skills-reduction.md) ([note](https://note.com/toshikiigaa/n/n8e8cd6897ed8))
- 2026-05-31: [生成AIのトークン消費量を抑える考え方](2026/05/20260531/20260531-token-consumption-02-reduction.md) ([note](https://note.com/toshikiigaa/n/n503c4a87077f))
- 2026-05-30: [生成AIとトークンの基本](2026/05/20260530/20260530-token-consumption-01-basics.md) ([note](https://note.com/toshikiigaa/n/n8e9122aaedef))

### 魔法比喩シリーズ

生成AI agent の周辺技術を「妖精さん」「魔法陣」「魔法書」の比喩で読む三部作です。確認順は新しい順、物語としての読み順は 2026-06-03 から 2026-06-06 です。

- 2026-06-06: [生成AI agent の向こう側には、いろいろな妖精さんがいる](2026/06/20260606/20260606-general-ai-agent-fairies-outline.md) ([note](https://note.com/toshikiigaa/n/ndc1b1eca21fc))
- 2026-06-05: [生成AIの MCP は、妖精さんへお願いする魔法陣に近い](2026/06/20260605/20260605-general-mcp-magic-circle-outline.md) ([note](https://note.com/toshikiigaa/n/n4d3a240982f2))
- 2026-06-03: [生成AIの Agent Skills は魔法書に近い](2026/06/20260603/20260603-general-agent-skills-magic-book.md) ([note](https://note.com/toshikiigaa/n/n118093b21838))

### Agent Skills

- 2026-05-29: [Agent Skills による開発資産の発芽成長](2026/05/20260529/20260529-agent-skills-development-assets-germination-growth.md) ([note](https://note.com/toshikiigaa/n/ne9593f75fccd))
- 2026-05-26: [Agent Skill を作っていて、BASIC とマシン語を思い出した](2026/05/20260526/20260526-agent-skills-basic-machine-language.md) ([note](https://note.com/toshikiigaa/n/n142354986e19))
- 2026-05-23: [コンテンツ型 Agent Skill にはどんな種類があるか](2026/05/20260523/20260523-content-agent-skill-types.md) ([note](https://note.com/toshikiigaa/n/n0ebcb626b082))
- 2026-05-16: [コンテンツ型 Agent Skill を活用してみる](2026/05/20260516/20260516-content-agent-skills.md) ([note](https://note.com/toshikiigaa/n/n72da1e228062))
- 2026-05-14: [Agent Skills 開発入門：自然言語でプログラミングするという考え方](2026/05/20260514/20260514-agent-skills-natural-language-programming.md) ([note](https://note.com/toshikiigaa/n/ned521551398c))
- 2026-05-09: [Agent Skills の発火は、どのように起きているのか](2026/05/20260509/20260509-agent-skills-activation.md) ([note](https://note.com/toshikiigaa/n/nfd0dda4c85b4))
- 2026-05-09: [Agent Skills では、説明ページの役割が少し変わる](2026/05/20260509/20260509-agent-skills-docs.md) ([note](https://note.com/toshikiigaa/n/n87a21add286b))

### 基礎知識・開発の考え方

Mermaid、Markdown、アジャイルなど、生成AI時代にも土台として読んでおきたい基礎知識や開発の考え方です。

- 2026-06-11: [生成AI時代のアジャイル：4つの価値に起きるパラダイムシフト](2026/06/20260611/20260611-general-ai-agile-values-shift.md) ([note](https://note.com/toshikiigaa/n/nf5c7d9583836))
- 2026-06-09: [アジャイルソフトウェア開発宣言からはじまるアジャイル入門](2026/06/20260609/20260609-general-agile-thinking.md) ([note](https://note.com/toshikiigaa/n/nb8814892039d))
- 2026-06-04: [Mermaid から入る UML 入門：図からクラス図・シーケンス図・状態遷移図をちょっと理解](2026/06/20260604/20260604-general-mermaid-uml-introduction.md) ([note](https://note.com/toshikiigaa/n/nf5c1c6c1d2c1))
- 2026-05-16: [Markdown 入門は、まず GitHub 風 Markdown から始めたい](2026/05/20260516/20260516-general-markdown-gfm-introduction.md) ([note](https://note.com/toshikiigaa/n/nc9c66635f525))

### 生成AI・AI agent

- 2026-06-13: [AI agent は速読する：しくみを知ってうまく付き合う開発スタイル](2026/06/20260613/20260613-general-ai-agent-speed-reading-dev-style.md) ([note](https://note.com/toshikiigaa/n/n5a3c4ef23c6a))
- 2026-06-01: [生成AIモデルの仕組み入門：トークン、ベクトル、Attention、学習](2026/06/20260601/20260601-general-generative-ai-model-vectors.md) ([note](https://note.com/toshikiigaa/n/ne5ef9e60e293))
- 2026-05-30: [生成AIは、なぜこんなに親しみやすい価格帯で使えてしまうのか](2026/05/20260530/20260530-general-ai-subscription-pricing-runway.md) ([note](https://note.com/toshikiigaa/n/nf26df188559a))
- 2026-05-28: [AI agent とキャラクター人格で技術エッセイを書くということ](2026/05/20260528/20260528-general-character-persona-technical-essay.md) ([note](https://note.com/toshikiigaa/n/ne68cf56c07f3))
- 2026-05-27: [OpenAI / Codex の UI を、公式名称と自分の理解に分けて整理してみる](2026/05/20260527/20260527-general-openai-codex-surfaces.md) ([note](https://note.com/toshikiigaa/n/n1234a1d255a9))
- 2026-05-27: [AI agent は、全部読まないのに、なぜ開発できるのか](2026/05/20260527/20260527-general-ai-agent-does-not-read-all-source.md) ([note](https://note.com/toshikiigaa/n/n80a82f70fe7c))
- 2026-05-15: [生成AI時代のアプリは、AIが理解・変更・検証できる単位に分ける](2026/05/20260515/20260515-general-ai-understand-change-verify-unit.md) ([note](https://note.com/toshikiigaa/n/n923232b6a9cd))
- 2026-05-14: [AI-native CLI / MCP / Agent Skills 設計メモ：AI が呼びやすいツールになるよう最初から設計する](2026/05/20260514/20260514-general-ai-native-cli-mcp-agent-skills.md) ([note](https://note.com/toshikiigaa/n/n2a4b7b75f0ee))
- 2026-05-14: [生成AI開発まわりの “Engineering” を整理してみる](2026/05/20260514/20260514-general-ai-engineering-overview.md) ([note](https://note.com/toshikiigaa/n/ne0b10ab8061a))
- 2026-05-10: [MCP は、生成AIに道具を渡すための入口になる](2026/05/20260510/20260510-general-mcp-server-client-local.md) ([note](https://note.com/toshikiigaa/n/ne87c899f68d2))
- 2026-04-30: [生成AI agent と開発するとき、README・docs・TODO は会話の外の記憶になる](2026/04/20260430/20260430-general-ai-dev-docs-todo.md) ([note](https://note.com/toshikiigaa/n/n5dcb66e47151))
- 2026-04-28: [生成AIと長く話していたら、日本語の使い方が少し変わってきた](2026/04/20260428/20260428-general.md) ([note](https://note.com/toshikiigaa/n/nca7cdb17f5db))

### miku 系ツール

- 2026-05-29: [miku-grep 開発日誌：AI agent に選ばれる CLI をそっと考察中](2026/05/20260529/20260529-general-ai-agent-cli-text-json.md) ([note](https://note.com/toshikiigaa/n/na7fb76c52fda))
- 2026-05-16: [[miku-text-bundle] 複数のテキストファイルを生成AI向け Markdown bundle に整理する](2026/05/20260516/20260516-miku-text-bundle-ai-text-assets.md) ([note](https://note.com/toshikiigaa/n/n5b18c376b2f0))
- 2026-04-28: [[miku-indexgen] AI にファイルを読ませる前に、まず地図が欲しかった話](2026/04/20260428/20260428-miku-indexgen-intro.md) ([note](https://note.com/toshikiigaa/n/n5b0ac55dce0a))
- 2026-04-12: [[miku-abc-player] `ABC` 記譜法の譜面を、ちょっと五線譜で見たくなった](2026/04/20260412/20260412-miku-abc-player-intro.md) ([note](https://note.com/toshikiigaa/n/n5be1d51d336a))
- 2026-04-12: [[mikuscore-skills] 生成AI に譜面対応させたくて、まず ABC 記譜法に寄っていった話](2026/04/20260412/20260412-ai-score-abc-first.md) ([note](https://note.com/toshikiigaa/n/n5362ea076328))
- 2026-04-10: [[mikuproject] WBS 作成を生成AIに手伝ってもらったら、思ったより幸せだった話](2026/04/20260410/20260410-mikuproject-agent-skills-wbs-planning.md) ([note](https://note.com/toshikiigaa/n/n87fd2d87bdf5))
- 2026-03-30: [[mikuproject] 生成AIと小さなツールを組み合わせたら、WBS の叩き台が意外とすんなりできた話](2026/03/20260330/20260330-mikuproject-ai-wbs-draft.md) ([note](https://note.com/toshikiigaa/n/nf5b9674d2cad))
- 2026-03-30: [[mikuproject] 作業を分けて並べた計画表を毎回ちがう形式で扱っているのが、だんだん気になってきた話](2026/03/20260330/20260330-mikuproject-intro.md) ([note](https://note.com/toshikiigaa/n/n20f5ee782358))
- 2026-03-27: [[xlsx2md] 設計書の取り消し線が Markdown で消えると、ちょっと危ない](2026/03/20260327/20260327-xlsx2md-strike-meaning.md) ([note](https://note.com/toshikiigaa/n/nc0f61d0f1bb2))
- 2026-03-26: [[xlsx2md] Excel 方眼を Markdown にする記事を書こうとしたら、およよとなった話](2026/03/20260326/20260326-xlsx2md-grid-bug-diary.md) ([note](https://note.com/toshikiigaa/n/ne63f03142852))
- 2026-03-20: [コードを書かずに、生成AIと一緒にアプリを作ってみた](2026/03/20260320/20260320-gpt54-app-dev.md) ([note](https://note.com/toshikiigaa/n/ncc28f9a0fcbd))

## 全記事一覧

| Date | Article | Published |
| --- | --- | --- |
| 2026-06-13 | [AI agent は速読する：しくみを知ってうまく付き合う開発スタイル](2026/06/20260613/20260613-general-ai-agent-speed-reading-dev-style.md) | [note](https://note.com/toshikiigaa/n/n5a3c4ef23c6a) |
| 2026-06-11 | [生成AI時代のアジャイル：4つの価値に起きるパラダイムシフト](2026/06/20260611/20260611-general-ai-agile-values-shift.md) | [note](https://note.com/toshikiigaa/n/nf5c7d9583836) |
| 2026-06-09 | [アジャイルソフトウェア開発宣言からはじまるアジャイル入門](2026/06/20260609/20260609-general-agile-thinking.md) | [note](https://note.com/toshikiigaa/n/nb8814892039d) |
| 2026-06-06 | [生成AI agent の向こう側には、いろいろな妖精さんがいる](2026/06/20260606/20260606-general-ai-agent-fairies-outline.md) | [note](https://note.com/toshikiigaa/n/ndc1b1eca21fc) |
| 2026-06-05 | [生成AIの MCP は、妖精さんへお願いする魔法陣に近い](2026/06/20260605/20260605-general-mcp-magic-circle-outline.md) | [note](https://note.com/toshikiigaa/n/n4d3a240982f2) |
| 2026-06-04 | [Mermaid から入る UML 入門：図からクラス図・シーケンス図・状態遷移図をちょっと理解](2026/06/20260604/20260604-general-mermaid-uml-introduction.md) | [note](https://note.com/toshikiigaa/n/nf5c1c6c1d2c1) |
| 2026-06-03 | [生成AIの Agent Skills は魔法書に近い](2026/06/20260603/20260603-general-agent-skills-magic-book.md) | [note](https://note.com/toshikiigaa/n/n118093b21838) |
| 2026-06-01 | [生成AIモデルの仕組み入門：トークン、ベクトル、Attention、学習](2026/06/20260601/20260601-general-generative-ai-model-vectors.md) | [note](https://note.com/toshikiigaa/n/ne5ef9e60e293) |
| 2026-05-31 | [note 記事一覧](2026/05/20260531/20260531-note-article-list.md) | [note](https://note.com/toshikiigaa/n/nde411c861a5a) |
| 2026-05-31 | [Agent Skills でトークン消費量を抑える考え方](2026/05/20260531/20260531-token-consumption-03-agent-skills-reduction.md) | [note](https://note.com/toshikiigaa/n/n8e8cd6897ed8) |
| 2026-05-31 | [生成AIのトークン消費量を抑える考え方](2026/05/20260531/20260531-token-consumption-02-reduction.md) | [note](https://note.com/toshikiigaa/n/n503c4a87077f) |
| 2026-05-30 | [生成AIとトークンの基本](2026/05/20260530/20260530-token-consumption-01-basics.md) | [note](https://note.com/toshikiigaa/n/n8e9122aaedef) |
| 2026-05-30 | [生成AIは、なぜこんなに親しみやすい価格帯で使えてしまうのか](2026/05/20260530/20260530-general-ai-subscription-pricing-runway.md) | [note](https://note.com/toshikiigaa/n/nf26df188559a) |
| 2026-05-29 | [miku-grep 開発日誌：AI agent に選ばれる CLI をそっと考察中](2026/05/20260529/20260529-general-ai-agent-cli-text-json.md) | [note](https://note.com/toshikiigaa/n/na7fb76c52fda) |
| 2026-05-29 | [Agent Skills による開発資産の発芽成長](2026/05/20260529/20260529-agent-skills-development-assets-germination-growth.md) | [note](https://note.com/toshikiigaa/n/ne9593f75fccd) |
| 2026-05-28 | [AI agent とキャラクター人格で技術エッセイを書くということ](2026/05/20260528/20260528-general-character-persona-technical-essay.md) | [note](https://note.com/toshikiigaa/n/ne68cf56c07f3) |
| 2026-05-27 | [OpenAI / Codex の UI を、公式名称と自分の理解に分けて整理してみる](2026/05/20260527/20260527-general-openai-codex-surfaces.md) | [note](https://note.com/toshikiigaa/n/n1234a1d255a9) |
| 2026-05-27 | [AI agent は、全部読まないのに、なぜ開発できるのか](2026/05/20260527/20260527-general-ai-agent-does-not-read-all-source.md) | [note](https://note.com/toshikiigaa/n/n80a82f70fe7c) |
| 2026-05-26 | [Agent Skill を作っていて、BASIC とマシン語を思い出した](2026/05/20260526/20260526-agent-skills-basic-machine-language.md) | [note](https://note.com/toshikiigaa/n/n142354986e19) |
| 2026-05-23 | [コンテンツ型 Agent Skill にはどんな種類があるか](2026/05/20260523/20260523-content-agent-skill-types.md) | [note](https://note.com/toshikiigaa/n/n0ebcb626b082) |
| 2026-05-16 | [[miku-text-bundle] 複数のテキストファイルを生成AI向け Markdown bundle に整理する](2026/05/20260516/20260516-miku-text-bundle-ai-text-assets.md) | [note](https://note.com/toshikiigaa/n/n5b18c376b2f0) |
| 2026-05-16 | [Markdown 入門は、まず GitHub 風 Markdown から始めたい](2026/05/20260516/20260516-general-markdown-gfm-introduction.md) | [note](https://note.com/toshikiigaa/n/nc9c66635f525) |
| 2026-05-16 | [コンテンツ型 Agent Skill を活用してみる](2026/05/20260516/20260516-content-agent-skills.md) | [note](https://note.com/toshikiigaa/n/n72da1e228062) |
| 2026-05-15 | [生成AI時代のアプリは、AIが理解・変更・検証できる単位に分ける](2026/05/20260515/20260515-general-ai-understand-change-verify-unit.md) | [note](https://note.com/toshikiigaa/n/n923232b6a9cd) |
| 2026-05-14 | [AI-native CLI / MCP / Agent Skills 設計メモ：AI が呼びやすいツールになるよう最初から設計する](2026/05/20260514/20260514-general-ai-native-cli-mcp-agent-skills.md) | [note](https://note.com/toshikiigaa/n/n2a4b7b75f0ee) |
| 2026-05-14 | [生成AI開発まわりの “Engineering” を整理してみる](2026/05/20260514/20260514-general-ai-engineering-overview.md) | [note](https://note.com/toshikiigaa/n/ne0b10ab8061a) |
| 2026-05-14 | [Agent Skills 開発入門：自然言語でプログラミングするという考え方](2026/05/20260514/20260514-agent-skills-natural-language-programming.md) | [note](https://note.com/toshikiigaa/n/ned521551398c) |
| 2026-05-10 | [MCP は、生成AIに道具を渡すための入口になる](2026/05/20260510/20260510-general-mcp-server-client-local.md) | [note](https://note.com/toshikiigaa/n/ne87c899f68d2) |
| 2026-05-09 | [Agent Skills では、説明ページの役割が少し変わる](2026/05/20260509/20260509-agent-skills-docs.md) | [note](https://note.com/toshikiigaa/n/n87a21add286b) |
| 2026-05-09 | [Agent Skills の発火は、どのように起きているのか](2026/05/20260509/20260509-agent-skills-activation.md) | [note](https://note.com/toshikiigaa/n/nfd0dda4c85b4) |
| 2026-04-30 | [生成AI agent と開発するとき、README・docs・TODO は会話の外の記憶になる](2026/04/20260430/20260430-general-ai-dev-docs-todo.md) | [note](https://note.com/toshikiigaa/n/n5dcb66e47151) |
| 2026-04-28 | [[miku-indexgen] AI にファイルを読ませる前に、まず地図が欲しかった話](2026/04/20260428/20260428-miku-indexgen-intro.md) | [note](https://note.com/toshikiigaa/n/n5b0ac55dce0a) |
| 2026-04-28 | [生成AIと長く話していたら、日本語の使い方が少し変わってきた](2026/04/20260428/20260428-general.md) | [note](https://note.com/toshikiigaa/n/nca7cdb17f5db) |
| 2026-04-12 | [[miku-abc-player] `ABC` 記譜法の譜面を、ちょっと五線譜で見たくなった](2026/04/20260412/20260412-miku-abc-player-intro.md) | [note](https://note.com/toshikiigaa/n/n5be1d51d336a) |
| 2026-04-12 | [[mikuscore-skills] 生成AI に譜面対応させたくて、まず ABC 記譜法に寄っていった話](2026/04/20260412/20260412-ai-score-abc-first.md) | [note](https://note.com/toshikiigaa/n/n5362ea076328) |
| 2026-04-10 | [[mikuproject] WBS 作成を生成AIに手伝ってもらったら、思ったより幸せだった話](2026/04/20260410/20260410-mikuproject-agent-skills-wbs-planning.md) | [note](https://note.com/toshikiigaa/n/n87fd2d87bdf5) |
| 2026-03-30 | [[mikuproject] 生成AIと小さなツールを組み合わせたら、WBS の叩き台が意外とすんなりできた話](2026/03/20260330/20260330-mikuproject-ai-wbs-draft.md) | [note](https://note.com/toshikiigaa/n/nf5b9674d2cad) |
| 2026-03-30 | [[mikuproject] 作業を分けて並べた計画表を毎回ちがう形式で扱っているのが、だんだん気になってきた話](2026/03/20260330/20260330-mikuproject-intro.md) | [note](https://note.com/toshikiigaa/n/n20f5ee782358) |
| 2026-03-27 | [[xlsx2md] 設計書の取り消し線が Markdown で消えると、ちょっと危ない](2026/03/20260327/20260327-xlsx2md-strike-meaning.md) | [note](https://note.com/toshikiigaa/n/nc0f61d0f1bb2) |
| 2026-03-26 | [[xlsx2md] Excel 方眼を Markdown にする記事を書こうとしたら、およよとなった話](2026/03/20260326/20260326-xlsx2md-grid-bug-diary.md) | [note](https://note.com/toshikiigaa/n/ne63f03142852) |
| 2026-03-20 | [コードを書かずに、生成AIと一緒にアプリを作ってみた](2026/03/20260320/20260320-gpt54-app-dev.md) | [note](https://note.com/toshikiigaa/n/ncc28f9a0fcbd) |

## Contents

Current article packages are listed in [記事をテーマ別に読む](#記事をテーマ別に読む)
and [全記事一覧](#全記事一覧).

Supporting documentation:

- `docs/repository-overview.md`: repository overview and current article theme.
- `docs/note-article-import-procedure.md`: procedure for importing Note articles.
- `docs/root-index-maintenance.md`: how to update root `index.json`.

Generated root index:

- `index.json`

The root index is generated by `miku-indexgen`. Do not edit it by hand.

## Directory Layout

```text
2026/
  YYYYMMDD/
    YYYYMMDD-article-slug.md
    images/
      000.jpg
      001.jpg
      src/
        image-prompt.md
        sections/
docs/
index.json
README.md
```

The exact image file names may differ by article. For example, the `20260606`
article uses `u000.png` style names, while the `20260605` article uses `000.jpg`
style names.

## Article Metadata

Article Markdown files should follow this front matter shape:

```yaml
---
title: 記事タイトル
tags: #生成AI #MCP #AIagent #PromptEngineering #mikuku
author: igapyon
published_to: note
writer_agent: みくく
url: https://note.com/toshikiigaa/n/example
release_date: YYYY-MM-DD
---
```

After front matter, place the article title as an H1, then the cover image:

```md
# 記事タイトル

![記事タイトル](images/000.jpg)
```

See `docs/note-article-import-procedure.md` for the full import procedure.

## Updating Root Indexes

Run this from the repository root after adding or changing articles or docs:

```sh
java -jar /Users/igapyon/.codex/skills/igapyon-miku-indexgen/runtime/miku-indexgen-1.4.4.jar \
  --input-directory . \
  --output-directory . \
  --title "mikuku-articles"
```

This updates `index.json`.

See `docs/root-index-maintenance.md` for maintenance details.

## Repository Hygiene

- Do not commit `.DS_Store`.
- Do not manually edit generated `index.json`.
- Keep image-generation prompts under each article's `images/src/` directory when
  they are part of the article package.
- Commit article Markdown, images, prompt sources, docs, and the refreshed root index
  together when they belong to the same import or maintenance task.
