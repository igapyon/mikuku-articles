# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: step2 で見えたこと
- section-text: sections/002/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Section Graphic Recording Text

## 見出し

step2 で見えたこと

## 主題

`index.json` で探索入口は改善したが、記事群の主張を答えるには raw 本文へ戻る必要がある。

## キーワード

- `miku-indexgen`
- `index.json`
- 探索の入口
- 消費量の揺れ
- 蒸留 Markdown は本文の代替ではない
- raw に戻る判断
- 観測として扱う

## 図解

```text
index.json あり
  ↓
入口は見つけやすい
  ↓
でも主張や根拠は raw で確認
```

## 観測

- `index.json` なし: 平均 約 110.6K used
- `index.json` あり: 平均 約 82.4K used
- 質問が「探す」だけでなく「考え方を整理する」場合、raw 本文が必要になる

## 注意点

- step3 は「トークン削減に成功した話」として扱わない
- 消費量だけではなく、意味構造と根拠確認の分離を見る
- 安定したとは断定せず、観察として扱う

## 吹き出し案

「入口はできました。でも、根拠は raw に戻って確認するのです…」

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
