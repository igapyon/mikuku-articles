# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: おわりに
- section-text: sections/007/section-text.md
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

# おわりに

## 主題

- GitHub公開状態から数えた Agent Skills は、2026年7月24日時点で28件
- 28件には、頻繁に使うもの、間接的に支えるもの、地味なもの、実験中のもの、育てたいものが含まれる
- これからも助かった手順や迷ったところを少しずつ Agent Skills に残していく

## 図解キーワード

- 28件
- 頻繁に使う
- 間接的に支える
- 実験中
- これから育てたい
- 次に同じところで立ち止まらない
- ひとつずつ

## 関係・流れ・対比

```text
28件の現在地を眺める
  ↓
頼っている道具と、次に育てたい道具が見える
  ↓
助かった手順・迷ったところを残す
  ↓
次に同じところで立ち止まらない
```

- すべてを均等に使う必要はない
- 今の作業と次の育成先を見つけるための一覧

## 図解構造

- layout-family: cycle
- primary-relation: 28件の現在地を把握し、頼っている道具と育てたい道具を見つけ、次の作業へ手順を残す循環

## グラレコ構図案

- 左: `28件` を中心に、`頻繁に使う`、`間接的に支える`、`実験中`、`これから育てたい` の4分類を小さくまとめる
- 中央: 最大の安心カード `全部を均等に使う必要はない`。そこから `今の作業で頼る道具` と `次に育てたい道具` の二方向へ分ける
- 右: `助かった手順を残す` → `次に立ち止まらない` の小さな循環とみくく。最後は明るい余韻にする
- みくくの表情・視線: 右側で少し照れながらも前向きな表情。中央の安心カードから右の循環へ視線を向ける。手は空にする
- 吹き出し: 「ひとつずつ、残していきます…」

## 正確性メモ

- 数値は `28件` と記事本文にある `2026年7月24日時点` の時点表現だけを使う
- 使われ方の分類は優劣やランキングにしない
- 将来の結果や件数を断定しない

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、中央の安心カードと右向き循環を最大化
- 背景は明るい白〜薄いアイボリーで全面不透明、文字は濃色、淡いアクセントのみ
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
sections/007/graphic-recording.png
```
