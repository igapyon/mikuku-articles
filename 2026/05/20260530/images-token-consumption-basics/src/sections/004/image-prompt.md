# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: 入力トークンと出力トークン
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 004 入力トークンと出力トークン

## 主題

トークン消費量は、入力側と出力側の両方で考える。

## キーワード

- 入力トークン
- 出力トークン
- 質問
- 会話履歴
- 添付ファイル
- 回答
- コード

## 図解の流れ

```text
質問・履歴・資料・ファイル
  ↓
入力トークン
  ↓
AIモデル
  ↓
出力トークン
  ↓
回答・説明・コード
```

## 注意点

- Markdown やテキストファイルは中身が入力になりやすい
- PDF、Word、Excel は抽出されたテキストや構造が入力になりうる
- 画像や音声も、対応モデルでは利用量と無関係とは限らない
- 短い質問と短い回答は軽くなりやすい
- 長い資料と長い出力は重くなりやすい

## みくく吹き出し案

「入力と出力、どちらでもトークンは増えるのです…」

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
