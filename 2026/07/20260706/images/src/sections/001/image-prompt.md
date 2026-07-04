# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 001. はじめに

## 主題

- Excel を Markdown へ変換する理由
- Word とは違う Excel の読み方
- miku-xlsx2md は「見た目再現」ではなく「読める入口」

## 図解キーワード

- Excel workbook
- Sheet / Cell / Table / Formula / Drawing
- 設計書、台帳、チェックリスト、設定表
- 人間の見た目判断
- AI agent が読みやすい Markdown

## 流れ

```text
Excel の中の情報
  ↓
表・地の文・数式・画像などを整理
  ↓
Markdown へ変換
  ↓
AI agent が参照しやすくなる
```

## 対比

| 見方 | 内容 |
| --- | --- |
| Word | 本文、見出し、表を読む |
| Excel | workbook、sheet、cell、formula、drawing を読む |
| 完全再現 | 目的ではない |
| 読める形 | 目的 |

## 吹き出し案

「あ、あの…Excel は表だけじゃなくて、設計書の入口にもなるのです…」

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
sections/001/graphic-recording.png
```
