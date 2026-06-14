# Section Graphic Recording Image Prompt

## Source

- section: 009
- title: 共通基盤を作るために、フィードバックを返す
- section-text: sections/009/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 009 共通基盤を作るために、フィードバックを返す

## 主題

- 生成AIのコンテキストと人間側の関心領域は最初から一致しない
- 言葉でフィードバックして、共通基盤を少しずつ作る

## 図解キーワード

- コンテキスト
- 関心領域
- 共通基盤
- グラウンディング
- 前提
- 方向
- 違和感
- 足場

## すり合わせの流れ

```text
人間側の関心領域
  ↓ 言葉にする
生成AI側のコンテキスト
  ↓ すり合わせ
共通基盤
```

## フィードバック例

- いいね
- そこは違う
- この方向で続けて
- 今の説明は近い
- もっと実務寄りにして

## まとめ

- 言葉にしない反応は伝わりにくい
- テキスト会話では、言葉にしたものが足場になる

## 吹き出し案

「言葉にしたものが、会話の足場になります…」

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
