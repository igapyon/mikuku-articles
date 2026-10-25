# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
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

# はじめに

## 主題

- 一つずつ作ってきた Agent Skills を、まず全体として数えてみる
- 結果は28件。ただし、すべてを同じ熱量で使っているわけではない
- 数だけでなく、頻繁に使うもの、間接的に働くもの、実験中のもの、育てたいものも見る

## 図解キーワード

- Agent Skills
- GitHub公開
- `SKILL.md`
- 28件
- 中央リポジトリ14件
- 専用リポジトリ14件
- 使われ方

## 関係・流れ・対比

```text
一つずつ作る小さな道具
  ↓ GitHub公開状態を見直す
`SKILL.md` を数える
  ↓
28件を、使われ方と一緒に眺める
```

- 入口は個別の小さな道具
- 到達点は数の把握と使われ方の整理

## 図解構造

- layout-family: flow
- primary-relation: 一つずつ作ってきた小さな Agent Skills を数え、使われ方も一緒に見る流れ

## グラレコ構図案

- 左: GitHub公開と小さな道具の入口。小さなラベルを数個だけ置き、`SKILL.md` へ向かう矢印を描く
- 中央: 大きな `28件` の円と、その下に `中央リポジトリ14件` / `専用リポジトリ14件` の短い内訳を置く
- 右: `使われ方` を4つの淡いカードで示す。`頻繁に使う`、`間接的に支える`、`実験的`、`これから育てたい`
- みくくの表情・視線: 右下で少し控えめに微笑み、中央の `28件` と右の使われ方カードを見る。手は空にする
- 吹き出し: 「まずは、全体を数えてみます…」

## 正確性メモ

- この章で使う数値は `28件`、`中央リポジトリ14件`、`専用リポジトリ14件` だけ
- 数え方の詳細や snapshot 日付は、この章の主図へ過剰に混ぜない
- Agent Skills の優劣や人気ランキングは示さない

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、中央の流れと `28件` を最大化
- 均一に明るい白〜ごく薄いアイボリー、濃色の文字、やわらかい手描き線
- みくくは1人、説明役として読める大きさ、物を持たず、短い吹き出しを1つ

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
sections/001/graphic-recording.png
```
