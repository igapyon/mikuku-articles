# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: AI アシスタントを作る、その少し手前
- section-text: sections/002/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# AI アシスタントを作る、その少し手前

## 主題

- Agent Builder や Gem Classic は、手元の資料から用途別の AI アシスタントを作れる。
- ファイル数が登録上限を超えると、資料を一つずつ登録できない。
- `miku-ai-assistant-builder-skills` は配備前の整理を担当する。

## 図解キーワード

- Knowledge
- 多数のファイル
- 登録上限
- ファイルをまとめる
- 配備前の準備

## 関係・流れ・対比

作りたい AI アシスタント ← 登録上限で詰まる ← 多数の資料

多数の資料 → 結合・整理 → 登録可能な件数

## グラレコ構図案

- 左: 整理済みだが数の多い Markdown、コード、メモ。
- 中央: 「登録上限」の狭い入口と、そこで詰まるファイル。
- 右: 少数へまとめられた Knowledge と AI アシスタント。
- みくくの表情・視線: 狭い入口を心配そうに見つつ、解決の矢印を案内する。
- 吹き出し: 「資料が入口を通れません…」

## 正確性メモ

- 問題の中心は資料の乱雑さではなく、ファイル数が登録上限を超えること。
- 具体的な上限数はこのセクションでは描かない。

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
sections/002/graphic-recording.png
```
