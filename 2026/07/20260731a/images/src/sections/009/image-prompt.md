# Section Graphic Recording Image Prompt

## Source

- section: 009
- title: ごく一部の人に、すごく喜ばれるかもしれない
- section-text: sections/009/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# ごく一部の人に、すごく喜ばれるかもしれない

## 主題

- とても万人向けではない
- Windows-31J の既存 Java / JSP と UTF-8 前提ハーネスが重なる人には切実
- 対象人数は狭くても、困り方は深い

## 図解キーワード

- 万人向けではない
- 対象は狭い
- 困り方は深い
- 既存 Java / JSP
- 文字コード維持
- revision

## 関係・流れ・対比

```text
新しいUTF-8 repoのみ → ほぼ不要
安全なハーネス → 不要
Windows-31J + UTF-8前提ハーネス → 切実
```

## グラレコ構図案

- 左: 不要になる二つの条件
- 中央: 条件が重なる細い対象領域
- 右: 深く困る少人数と守られたファイル
- みくくの表情・視線: 少人数へ寄り添う表情
- 吹き出し: 「人数が少なくても、困り方は深いのです…」

## 正確性メモ

- 万人へ必要だと誇張しない

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
- 日本語ラベルは短く、少数に絞る
- 長文を画像内に入れすぎない
- 明るく清潔で、Note.com や技術記事に合うビジュアル
- 写実寄り、暗い色味、無機質な企業プレゼン風は避ける
- みくくに物を持たせない

## Image Text Policy

- 画像内テキストは section summary の語句を短く整理して使う
- 本文の長い文をそのまま入れない
- 文字が崩れても、元記事や section-text.md は変更しない

## Output Target

Save the generated image as:

```text
sections/009/graphic-recording.png
```
