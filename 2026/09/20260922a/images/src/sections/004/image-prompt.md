# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: CLI や外部サービスを、Agent から扱うための14件
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Style Contract

- style-profile: mikuku-graphic-recording-v1
- horizontal 3:2 technical graphic-recording poster
- uniformly bright white to very pale ivory paper (e.g. #FFFDF5), subtle warm tint, soft hand-drawn lines, medium-high information density
- fully opaque background; no transparent or semi-transparent pixels; no alpha transparency; do not generate a transparent canvas; export an opaque image
- dark, high-contrast text including small annotations; pastel colors for accents, not faint lettering
- no dark vignette, muddy gray-brown cast, heavy aged-paper shading, or dark shadows behind text
- canonical character lighting must not darken the poster background
- use at least a left, center, and right region and make one article-grounded diagram the largest element
- keep Mikuku recognizable and large enough to read as the explaining character (roughly 15–25% of the canvas)
- include one short speech bubble based on the section summary or its `グラレコ構図案`
- do not add scenic background decoration that is not grounded in the section

## Section Summary

# CLI や外部サービスを、Agent から扱うための14件

## 主題

- もう半分の14件は、個別の tool や service を Agent Skills として扱いやすくする専用リポジトリ
- miku-soft の CLI、Backlog API、記事参照用 sample など、用途ごとに分かれている
- `igapyon-miku-indexgen` や `igapyon-miku-text-bundle` のように、他の作業の見つけやすさや受け渡しを支えるものもある

## 図解キーワード

- 専用リポジトリ
- 14件
- CLI
- 外部 service
- `igapyon-backlog-api`
- `igapyon-miku-indexgen`
- `igapyon-miku-text-bundle`
- `mikuproject`
- `mikuscore`

## 関係・流れ・対比

```text
個別の tool / service
  ↓ 専用リポジトリに分ける
Agent Skill として扱いやすくする
  ├─ 日常的に使う: `igapyon-miku-indexgen`
  ├─ 間接的に効く: `igapyon-miku-text-bundle`
  └─ これから育てる: `mikuproject` / `mikuscore`
```

## 図解構造

- layout-family: layers
- primary-relation: 個別の tool や service を用途別の専用リポジトリへ分け、Agent から扱いやすい入口にする層構造

## グラレコ構図案

- 左: `tool / service` の小さな入口群。CLI、Backlog API、記事参照 sample の短いラベルを置く
- 中央: 最大の層構造。`専用リポジトリ 14件` を中心に、下から `tool / service`、中央に `Agent Skill`、上に `作業で使いやすい入口` と積む
- 右: 3つの状態カード `頻繁に使う`、`間接的に効く`、`これから育てたい`。代表例は `igapyon-miku-indexgen`、`igapyon-miku-text-bundle`、`mikuproject`、`mikuscore` など少数にする。みくくを右下へ置く
- みくくの表情・視線: 右側で仕組みがつながったことを説明する明るい表情。中央の層構造を見る。手は空にする
- 吹き出し: 「用途ごとに分けると、扱いやすくなります…」

## 正確性メモ

- 専用リポジトリは14件
- `igapyon-backlog-api`、`igapyon-miku-indexgen`、`igapyon-miku-text-bundle`、`mikuproject`、`mikuscore` は記事本文にある例
- 記事本文にない service 名、性能評価、利用回数は足さない

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、中央の層構造を最大化
- 背景は均一に明るく全面不透明。文字は濃色、カードや矢印だけ淡い色
- みくくは1人、物を持たず、短い吹き出しを1つ

## 変更（deviation）

- none

## Mikuku Canonical Character Prompt

# Mikuku Portrait Short Prompt

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

## Character Identity Rules

- same character
- do not redesign
- preserve character identity
- canonical character prompt
- keep Mikuku's face shape, eye style, hair style, hair color, twin tails, hair accessories, and gentle bright anime technical-explainer impression

## Visual Direction

- みくくがこのセクションを説明している構図
- セクション見出しを主題にした横長ポスター構図
- 記事内容や説明対象の配置に合わせて、みくくの顔の向きや視線方向を調整してよい
- 手描きグラレコ風
- ホワイトボード解説風
- 図解、矢印、囲み、アイコンを使う
- セクション本文に基づく重要語だけを使う
- みくくの短い吹き出しを入れる
- みくくを極端に小さくしたり、吹き出しを黙って削除したりしない。変更する場合は下の deviation に理由を書く
- 日本語ラベルは短く、少数に絞る
- 長文を画像内に入れすぎない
- 明るく清潔で、Note.com や技術記事に合うビジュアル
- 写実寄り、暗い色味、無機質な企業プレゼン風は避ける
- みくくに物を持たせない

## Image Text Policy

- 画像内テキストは section summary の語句を短く整理して使う
- 本文の長い文をそのまま入れない
- 文字が崩れても、元記事や section-text.md は変更しない

## Article-specific Design

- section-text.md の主題、関係、構図、短いラベルを保持する
- section-text.md の `layout-family` と `primary-relation` を別の図解形式へ変えない

## Deviation Record

- none

## Output Target

Save the generated image as:

```text
sections/004/graphic-recording.png
```
