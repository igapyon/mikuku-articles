# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: 完成とは言わず、ゆっくり動作検証していた
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 完成とは言わず、ゆっくり動作検証していた

## 主題
- 最初の形を完成とせず、実例へ適用しながらレビュー品質を確認した。
- 機械的なテストだけでなく、人間がレビュー結果を読む必要がある。

## 図解キーワード
- ゆっくり検証
- 対象
- 目的
- モデル
- Context
- 根拠
- 過剰評価
- 人間の確認

## 関係・流れ・対比
一般プログラム: 入力 → 処理 → 期待出力
生成AIレビュー: 文章＋目的＋Context → 意味判断 → 人間が結果確認 → 再調整

## グラレコ構図案
- 左: 「完成？」の旗にいったん立ち止まる場面。
- 中央: 実例適用と結果確認の循環矢印。
- 右: 機械テストと人間レビューの二層チェック。
- みくくの表情・視線: 循環図を慎重に見守る表情。
- 吹き出し: 「レビュー結果もレビューします」

## 正確性メモ
- 再現性のない断定や数値を加えない。
- 観点数が多いほど良い、とは描かない。

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
