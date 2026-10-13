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

- GPT-5.6 Lunaの安さを出発点に、GPT-6でさらに下がった価格を見ていく。
- 比較対象は2026年10月10日時点のAPI料金。定額プランとは分ける。
- 価格変化をきっかけに、モデル選択の仮説も見直す。

## 図解キーワード

- GPT-5.6 Luna
- GPT-6 Luna
- さらに安い
- API料金
- 定額プランとは別
- 2026年10月10日時点

## 関係・流れ・対比

`GPT-5.6 Lunaも安い → GPT-6 Lunaはさらに安い → 価格とモデル選択を見直す`

## 図解構造

- layout-family: flow
- primary-relation: GPT-5.6 Lunaの安さを起点に、GPT-6の価格とモデル選択を見直す

## グラレコ構図案

- 左: 「GPT-5.6 Luna」「もう十分安い？」の気づき。
- 中央: GPT-5.6からGPT-6へ向かう「さらに安い」の矢印。具体価格はこの節にないため描かない。
- 右: 「API料金」「2026年10月10日時点」と、定額プランと区別する小さな注記。みくくは矢印を見る。
- みくくの表情・視線: 少し驚きつつ考える表情で、価格の変化へ視線を向ける。
- 吹き出し: 「Lunaは、次の世代でもっと安くなったのですね…！」

## 正確性メモ

- この節に具体的な価格はない。数値を補わない。
- API料金とCodex / ChatGPTの定額プラン利用枠を混同しない。
- 記事本文に明記された日付とモデル名だけを使う。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右の3領域、主図を最大化
- みくくは説明役として読める大きさで1人、短い吹き出しを1つ、物を持たない
- 背景は均一に明るい白〜ごく薄いアイボリーで全面不透明。濃色文字、淡い暖色の手描き線。

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
