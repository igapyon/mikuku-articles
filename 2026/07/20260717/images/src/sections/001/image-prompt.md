# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# はじめに

## 主題

約2か月の更新を順番にたどり、miku-text-bundleがどこを強化してきたかを記録する開発日誌。

## 図解キーワード

- 2026年5月16日: v0.8.1
- 約2か月の小さな改善
- 2026年7月16日: v1.5.1
- 出力構成・AIへの受け渡し・事前確認・Part分割
- 初めての人にも短い全体像

## 関係・流れ・対比

左の「v0.8.1」から右の「v1.5.1」へ、日付入りの手描きタイムラインを伸ばす。途中に小さな改善の付箋を並べ、更新の積み重ねが道具の役割を変えてきたことを示す。

## グラレコ構図案

- 左: 2026/5/16、v0.8.1、最初の記事を示すノート
- 中央: 約2か月の道のりと4つの改善テーマ
- 右: 2026/7/16、v1.5.1と「現在の姿」
- みくく: 右下で少し緊張しつつ案内する表情。視線はタイムライン中央へ
- 吹き出し: 「ひとつずつ、たどります」

## 正確性メモ

- 今回の対象は2026年5月17日以降の変更。
- 基本機能を一から詳説する記事ではなく、強化内容中心の開発日誌。
- 初見読者向けの全体像も短く扱う。

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
sections/001/graphic-recording.png
```
