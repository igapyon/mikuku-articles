# Section Graphic Recording Image Prompt

## Source

- section: 010
- title: 魔法書、魔法陣、妖精さん
- section-text: sections/010/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 010: 魔法書、魔法陣、妖精さん

## 主題

Agent Skills、MCP、妖精さんは役割が違う。分けて見ると生成AI agent の作業が立体的に見える。

## 三つの比喩

| 比喩 | 技術的な姿 | 役割 |
| --- | --- | --- |
| 魔法書 | Agent Skills | 前提、文体、手順、判断基準 |
| 魔法陣 | MCP | 外へお願いを届ける通り道 |
| うさぎ型の妖精さん | CLI / API / DB / internal function | 魔法陣の向こう側で働く |

## 図解

```text
魔法書
  ↓ 使い方を支える
agent
  ↓
魔法陣
  ↓
うさぎ型の妖精さん
```

## 注意点

- 魔法書だけでは外の道具へ届かない
- 魔法陣だけでは使いどころが曖昧
- 妖精さんだけでは入口や作法が足りない

## 吹き出し

「三つを分けると、どこで何が起きているか見えます…」

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
sections/010/graphic-recording.png
```
