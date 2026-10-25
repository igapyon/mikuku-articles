# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: 多数のファイルから配備用データを準備する
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 多数のファイルから配備用データを準備する

## 主題

- 多数のテキストファイルを少数の Knowledge 向け Markdown へバンドルする。
- Agent Builder 向けには Markdown を DOCX へ変換する。
- `upload/` と、名前・説明・Instructions などの設定用 Markdown を準備する。

## 図解キーワード

- miku-text-bundle
- 少数の Markdown
- miku-md2docx
- DOCX
- upload/
- 設定用 Markdown

## 関係・流れ・対比

多数のテキスト → `miku-text-bundle` → 少数の Knowledge Markdown

Agent Builder: Markdown → `miku-md2docx` → DOCX

Gem Classic: Markdown のまま／DOCX を選択

## グラレコ構図案

- 左: 相対パスと境界を持つ多数のテキストファイル。
- 中央: 上段にバンドル、下段に DOCX 変換の二つの工程。
- 右: `upload/` と設定用 Markdown、その先に Agent Builder と Gem Classic。
- みくくの表情・視線: 中央の変換フローを見て、丁寧に順路を説明する。
- 吹き出し: 「まとめて、渡せる形へ」

## 正確性メモ

- 多数のファイルを少数へまとめ、Markdown を DOCX へ橋渡しするのが主要機能。
- 自動アップロードや共有は行わない。
- みくくには物を持たせない。

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
