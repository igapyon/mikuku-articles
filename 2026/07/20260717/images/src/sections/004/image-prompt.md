# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: handoff出力を、少なく、分かりやすくする
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# handoff出力を、少なく、分かりやすくする

## 主題

生成AIへ渡す順番を明確にし、管理するファイル数と会話中の迷いを減らすhandoff出力の改善。

## 図解キーワード

- 読み込み順を固定
- filename prefix
- YAML front matter
- promptとindexをPartへ同梱
- 中間Partは「OK」のみ
- Markdown自身が読み方を伝える

## 関係・流れ・対比

左で旧構成のprompt＋複数Part＋indexを示し、中央で整理、右でPartだけのcompact出力へ変化させる。Part 1にprompt、最終Partにindex、中間Partにacknowledgement footerを示す。

## グラレコ構図案

- 左: ファイルが多く順番に迷う旧handoff
- 中央: 順序・prefix・metadataの整理
- 右: Part 1→Part 2→最終Partの簡潔な列
- みくく: 右下でファイルを順番どおり差し出す姿。視線は矢印へ
- 吹き出し: 「この順番で、どうぞ」

## 正確性メモ

- v1.1.0以降は独立したprompt/indexを廃止しPartへ同梱。
- 中間Partの案内は最終Part前の分析を抑え、OKのみを促す。
- 標準出力ではなく生成Markdownが受け渡しの正本。

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
