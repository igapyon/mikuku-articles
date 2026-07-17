# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: v0.8.1からv1.5.1までの流れ
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# v0.8.1からv1.5.1までの流れ

## 主題

2026年5月から7月まで、小さな違和感を一つずつ直しながら「生成AIへ誤解なく渡す出力契約」を整えた更新の流れ。

## 図解キーワード

- v0.9.0 読み込み順
- v1.0.x prefix・help・metadata
- v1.1.x compact出力
- v1.2.0 dry-run
- v1.3.0 Part分割
- v1.4.0 固定上限撤廃
- v1.5.x Knowledge source

## 関係・流れ・対比

左から右へのバージョンロードマップ。個別の変更を小さな道標として並べ、終点を「どこへ、どの契約で渡すか」に置く。

## グラレコ構図案

- 上: v0.8.1→v1.5.1の一本のロードマップ
- 中央: 主要な節目を7つの短いラベルで配置
- 下: 「使う→違和感を発見→直す」の循環矢印
- みくく: 左下から道を振り返る、少し驚いた表情
- 吹き出し: 「小さな改善の積み重ねです」

## 正確性メモ

- 対象期間のNode.js版はv0.9.0からv1.5.1。
- 各公開日よりも、変更の流れと意味を中心にする。
- v1.5.1はNode.js単一ファイルCLI bundle固有の修正だが、詳細説明は主題にしない。

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
