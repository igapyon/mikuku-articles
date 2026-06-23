# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: Qwen3 には、どんな Markdown を渡すとよいのだろう
- section-text: sections/006/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 006 Qwen3 には、どんな Markdown を渡すとよいのだろう

## 主題

Qwen3 には、粗い素材 Markdown の手前に蒸留 Markdown を置くと安定しやすい。

## 蒸留の意味

ここでの蒸留はモデル学習ではない。

**人間と AI agent が同じ全体像を見るための文脈整理。**

## 意味の地図

- すべての道を描きすぎない
- 迷いやすい場所を示す
- 戻るべき元資料を示す
- 未確定部分を明示する

## 蒸留 Markdown の構成例

- 中心概念
- 現行仕様として見えること
- 観測された差分
- まだ断定できないこと
- 元資料へ戻るべき場合
- 注意点

## 図解ポイント

```text
古い設計書 + ソース + DB
        ↓
蒸留 Markdown
        ↓
人間と agent の共通地図
```

## 吹き出し案

「机に積むだけでなく、作業順に並べておく感じです…」

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
sections/006/graphic-recording.png
```
