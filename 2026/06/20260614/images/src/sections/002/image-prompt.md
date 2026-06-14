# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: いきなり生成するのではなく、発掘する
- section-text: sections/002/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# いきなり生成するのではなく、発掘する

## 主題

ソースコード全体を AI agent に一気に読ませるのは重すぎる。まず人間が理解しやすい見取り図を作る。

## 図解キーワード

- 一気読みは重い
- トークン消費
- 時間がかかる
- 出力が期待と違う
- 情報量と理解しやすさは別
- 見取り図
- 最初の遺構

## 対比

| いきなり全部 | まず発掘 |
| --- | --- |
| 全ソースを背負う | 見える入口から読む |
| 情報過多 | 小さな見取り図 |
| 完成版を期待 | 仮説から始める |

## 図の流れ

```text
巨大なソースコード
  ↓ そのままでは重い
見えている遺構
  ↓
小さな地図
  ↓
次に読む場所が決まる
```

## 吹き出し案

「情報量が多いことと、理解しやすいことは別なのです…」

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
sections/002/graphic-recording.png
```
