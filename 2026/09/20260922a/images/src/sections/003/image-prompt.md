# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: 個人 workflow を支える14件
- section-text: sections/003/section-text.md
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

# 個人 workflow を支える14件

## 主題

- 中央リポジトリには、個人 workflow を支える Agent Skills が14件ある
- 書く、GitHubを扱う、リポジトリを保つ、みくくとして作業するなどの型を含む
- 頻繁に使うものだけでなく、間接的に支えるもの、ほとんど使わないもの、実験的なものもある

## 図解キーワード

- 中央リポジトリ
- 14件
- 個人 workflow
- `igapyon-miku-scm`
- `igapyon-mikuku-agent`
- `igapyon-note-writer`
- `igapyon-repo-conventions`
- `igapyon-skill-compactor`

## 関係・流れ・対比

```text
中央リポジトリ 14件
  ├─ 普段の作業の型
  │   ├─ 書く / GitHub / リポジトリ運用
  │   └─ みくくとして作業する
  ├─ 間接的に支える
  └─ ほとんど使わない・実験的
```

- `igapyon-miku-scm`、`igapyon-mikuku-agent` は頻繁に使う例
- `igapyon-note-writer`、`igapyon-repo-conventions` は間接的に頻繁に支える例
- companion系、`igapyon-diary-writer`、`igapyon-skill-compactor` はほとんど使わない・実験的な例

## 図解構造

- layout-family: cards
- primary-relation: 中央リポジトリ14件を、普段の workflow、間接的な支援、ほとんど使わない・実験的という使われ方のカードへ分ける

## グラレコ構図案

- 左: `中央リポジトリ` と大きな `14件`。下に「書く / GitHub / リポジトリ / みくく」の4つの小さな役割タグを置く
- 中央: 最大の3分類カード。`頻繁に使う`、`間接的に支える`、`ほとんど使わない・実験的` を横または縦に並べ、各カードに記事内の代表例を少数だけ置く
- 右: `使う回数だけが価値ではない` という短い補助ラベルとみくく。みくくは中央カードを見て説明する
- みくくの表情・視線: 右側で少し困り顔だが、見えにくい支えにも気づいてほしいという優しい表情。中央の分類カードを見る。手は空にする
- 吹き出し: 「前面に出ない道具も、支えてくれます…」

## 正確性メモ

- 中央リポジトリの数は14件
- 代表例は記事本文の Agent Skill 名だけを使う
- 「頻繁に使う」「間接的に支える」「ほとんど使わない・実験的」は記事の使われ方の分類で、優劣やランキングではない

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、分類カードの主図を最大化
- 均一に明るい不透明な白〜薄いアイボリー、淡いパステルはカードの塗りだけに使う
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

Additional character constraint for this section: show exactly one actual Mikuku character. Do not draw a second Mikuku avatar, chibi, face, twin-tail icon, or character portrait in any small role card; represent the `みくくとして作業する` role with a generic workflow icon or text only.

## Output Target

Save the generated image as:

```text
sections/003/graphic-recording.png
```
