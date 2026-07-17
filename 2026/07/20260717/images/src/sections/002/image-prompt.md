# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: はじめての方へ：miku-text-bundleとは
- section-text: sections/002/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# はじめての方へ：miku-text-bundleとは

## 主題

散らばったテキストを、ファイル境界を保ったまま、渡し先に合う分割Markdownへ整理するCLIツール。

## 図解キーワード

- README・設計資料・TODO・ソースコード
- 収集・除外・順序・文字コード・サイズ制限
- ファイル境界を保持
- handoff
- knowledge-source

## 関係・流れ・対比

左の散らばった複数ファイルが中央のmiku-text-bundleを通り、右で2本に分岐する。上は会話用のhandoff、下は中立的なKnowledge source。共通の土台は収集・除外・分割。

## グラレコ構図案

- 左: 種類の違うファイルが散らばる机
- 中央: 静かに整える箱「miku-text-bundle」
- 右上: handoff「順番・応答指示あり」
- 右下: knowledge-source「会話用指示なし」
- みくく: 中央下で荷物を包むような仕草。視線は2つの渡し先へ
- 吹き出し: 「渡す前に、整えます」

## 正確性メモ

- 指定ディレクトリ以下のテキストファイルを収集するCLI。
- 出力はファイル境界を保った分割Markdown。
- handoffとknowledge-sourceの2モードがある。

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
