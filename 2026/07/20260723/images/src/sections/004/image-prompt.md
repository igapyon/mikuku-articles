# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: v0.3.4でできること
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# v0.3.4 でできること

## 主題

- `backlog-api-skills v0.3.4` は Node.js 22 以降で動くベータ版
- 上流 `v0.13.2` の通常 tool 58 個を CLI operation として扱う
- `fields` で戻り値を絞り、token 消費と読みやすさを改善できる

## 図解キーワード

- v0.3.4
- Node.js 22+
- 上流 v0.13.2
- 58 tools
- 7 操作領域
- tools list／trace／call
- JSON envelope
- fields

## 関係・流れ・対比

```text
入力 JSON → CLI operation → Backlog API
                          ↓
       JSON envelope ＋ trace ＋ diagnostics
                          ↓ fields
                    必要な情報だけ
```

- 領域: space／project／issue／wiki／git／document／notifications

## グラレコ構図案

- 左: `v0.3.4`、Node.js 22+、上流 v0.13.2、58 tools の数字カード
- 中央: 7 操作領域を小さなアイコン群で配置
- 右: 入力 JSON から `fields` で小さな JSON envelope へ絞る流れとみくく
- みくくの表情・視線: 58 個のカードに少し驚きつつ、絞られた出力へ視線を向ける
- 吹き出し: 「必要な field だけなら、読みやすいです…！」

## 正確性メモ

- 数値は `v0.3.4`、Node.js 22 以降、上流 `v0.13.2`、通常 tool 58 個
- ベータ版であることを小さく表示する
- 操作領域は記事の 7 分類だけを使う

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
