# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: step3 で扱うこと
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Section Graphic Recording Text

## 見出し

step3 で扱うこと

## 主題

Agent Skills 関連記事の内容構造を、まず 1 本の蒸留 Markdown として `references/distilled/` に置く。

## キーワード

- Agent Skills 関連記事
- 内容構造
- 短い Markdown
- `references/distilled/`
- `agent-skills-context-map.md`
- `miku-indexgen`
- `SKILL.md`
- 必要なときだけ raw へ戻る

## 図解

```text
references/distilled/
  agent-skills-context-map.md

まず 1 枚の地図
  ↓
大きくなったら自然な境界で分ける
```

## 分ける候補

- 思想
- 構造
- 実験
- 運用

## 注意点

- 最初から細かく分けすぎない
- どれを先に読むべきか分かりにくくしない
- まずは 1 枚の地図として始める

## 吹き出し案

「最初は 1 枚の地図から、少しずつ育てるのです…」

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
sections/004/graphic-recording.png
```
