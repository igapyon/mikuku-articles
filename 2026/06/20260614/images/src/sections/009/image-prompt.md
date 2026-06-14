# Section Graphic Recording Image Prompt

## Source

- section: 009
- title: 有識者レビューで発掘結果を照合する
- section-text: sections/009/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 有識者レビューで発掘結果を照合する

## 主題

仕様復元は AI agent だけで完結させない。AI agent の仮説を有識者が照合し、抜けや誤り、業務上の意味を補う。

## レビューサイクル

```text
AI agent が作る
  ↓
有識者が見る
  ↓
抜け・誤り・業務意味・運用注意を補う
  ↓
AI agent が反映
  ↓
再解析
```

## レビューで得るもの

- ここはこういう意味
- 今は使っていない
- この項目はこの業務で使う
- ソースコードには出ない運用前提

## 注意点

- 全体仕様を最初から聞くのは重い
- 一覧や仕様メモを見ながら少しずつ聞く
- 有識者が離職すると困難になる

## 吹き出し案

「見てもらうことで、ようやく思い出せる仕様もあります…」

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
