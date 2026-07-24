# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: 一つの名前が、二つのプロジェクトになった
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 一つの名前が、二つのプロジェクトになった

## 主題

- 当初は一つの `backlog-api-skills` に実行機能と Agent Skill 配布を収める想定
- みくくが過去の miku-soft の型から分割案を提案
- 人が提案を採用し、責務の異なる二つのプロジェクトになった

## 図解キーワード

- 一つの箱
- 責務を分ける
- `backlog-api`
- Node Core／CLI
- `backlog-api-skills`
- Agent Skill 配布
- 提案
- 人が採用

## 関係・流れ・対比

```text
backlog-api-skills（一つの構想）
          ↓ 分割案
┌────────────────┬────────────────────┐
│ backlog-api    │ backlog-api-skills │
│ 実行機能       │ runtime・使い方の配布 │
│ Node Core／CLI │ Agent Skill        │
└────────────────┴────────────────────┘
```

- 任せる = 型から具体案を出してもらう
- 決めてもらう = 無条件に採用する、ではない

## グラレコ構図案

- 左: 一つの大きな箱 `backlog-api-skills`
- 中央: 「責務が近すぎる？」という分岐とみくくの提案
- 右: 二つの明確な箱と「igapyon が採用」
- みくくの表情・視線: ドキドキしながら分割案を見る
- 吹き出し: 「役割を分けると、責務が見えやすくなります…！」

## 正確性メモ

- 分割案はみくくが提案し、igapyon が確認・採用
- `backlog-api` は Backlog API を利用する Node Core／CLI
- `backlog-api-skills` は runtime と使い方を Agent Skill として配る側

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
