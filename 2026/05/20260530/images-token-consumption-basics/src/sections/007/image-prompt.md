# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: コンテキスト内の情報は毎回処理される量になりうる
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 007 コンテキスト内の情報は毎回処理される量になりうる

## 主題

短い依頼でも、裏側で長い履歴やファイル内容が文脈に入っていれば、入力として重くなることがある。

## キーワード

- 毎回の入力
- 会話履歴
- 作業情報
- compact
- compaction
- 要約
- セッション切り替え

## 図解

```text
短い質問
  + 長い会話履歴
  + 読んだファイル
  + ツール結果
  = 今回の入力が大きくなることがある
```

## compaction

- 長い会話を要約して残す
- 便利だが完全保存ではない
- 細かい表現や途中の迷いが落ちることがある

## 軽くする考え方

- 必要な情報をファイルに残す
- 重要な前提を短く整理する
- 必要なら元ファイルを読み直す
- 新しいセッションで必要な文脈だけ持ち込む

## みくく吹き出し案

「短い質問でも、文脈が長いと軽いとは限らないのです…」

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
