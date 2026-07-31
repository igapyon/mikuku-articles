# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: 仕方なく、専用の入口を作った
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 仕方なく、専用の入口を作った

## 主題

- 理想はハーネス自身が repository の文字コード規則を理解すること
- 改善を待てないため、AI agent とファイルの間へ専用 CLI を置いた
- 大きな仕組みを置き換えず、苦手なところだけ渡る「小さな橋」

## 図解キーワード

- 理想
- 現実
- 専用 CLI
- Agent Skill
- 小さな橋
- 必要なところだけ

## 関係・流れ・対比

```text
理想: ハーネスが直接、安全に扱う
現実: AI agent → Agent Skill → 専用 CLI → ローカルファイル
```

## グラレコ構図案

- 左: AI agent と「将来の改善」
- 中央: 苦手な区間だけを渡す小さな橋
- 右: Windows-31J の既存ファイル
- みくくの表情・視線: 少し不本意そうだが橋を見守る
- 吹き出し: 「壊すより、小さな橋を増やします…」

## 正確性メモ

- `miku-text-file-ops` はファイル操作、Skills は AI agent から選ぶ入口

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
