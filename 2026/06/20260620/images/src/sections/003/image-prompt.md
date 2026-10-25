# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: 回答手順からコンテキストへ
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Section Graphic Recording Text

## 見出し

回答手順からコンテキストへ

## 主題

生成AIへ細かい回答手順を渡す設計から、考えるための良いコンテキストを整える設計へ移る。

## キーワード

- 回答手順
- 回答テンプレート
- よく整理されたコンテキスト
- 事実
- 概念同士の関係
- 背景
- 制約
- 未確定点
- 参照すべき根拠

## 図解

```text
昔寄り:
  この順番で答える
  この型で分類する
  最後はこう締める

今寄り:
  事実
  関係
  背景
  制約
  根拠
```

## 対比

| 回答手順 | コンテキスト |
| --- | --- |
| AI に答え方を教える | AI と人間が資料群を見渡す |
| 外から骨格を与える | 材料を整理する |
| メタ情報が増えやすい | 能力を自然に引き出す |

## 吹き出し案

「答え方を縛るより、考える材料を整えるのかもしれません…」

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
sections/003/graphic-recording.png
```
