# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: 責めるより、分けて伝える
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 007 責めるより、分けて伝える

## 主題

- 「責める」より「分けて伝える」ほうが応答は安定しやすい
- 問題点、理由、確認順序を明確にすると、検証と修正に向かいやすい

## 図解キーワード

- 期待と違う
- Aの前提
- Bの確認
- 問題点を分解
- 修正方針
- 反論
- 留保
- 代替案

## Before / After

```text
これはダメ。ちゃんとやって。
  ↓
謝罪・迎合に寄りやすい

この部分は期待と違います。
理由は A と B です。
まず A、そのあと B を確認してください。
  ↓
確認・検証・修正に向かう
```

## まとめ

- 人間側の言い方が、次の応答の形を作る
- 人間扱いではなく、対話を壊さないための会話設計

## 吹き出し案

「責めるより、どこを直すか分けて渡します…」

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
sections/007/graphic-recording.png
```
