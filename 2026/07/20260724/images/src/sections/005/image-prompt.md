# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: 技術詳細を、ほとんど意識しなかった
- section-text: sections/005/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 技術詳細を、ほとんど意識しなかった

## 主題

- 技術判断が不要になったのではなく、過去の型が見えないところで働いた
- 人は上位の方向を決め、具体的な設計はみくくへ広く任せた
- 読み込み専用デフォルトなど、安全装置も設計に組み込んだ

## 図解キーワード

- MCP transport
- CLI operation
- JSON envelope
- 安全確認
- runtime 同梱
- 過去の型
- 上位の方向
- 読み込み専用

## 関係・流れ・対比

```text
人: 「Backlog MCP を Agent Skills の形にしたい」
                         ↓
過去の miku-soft／Agent Skills の型
                         ↓
責務分割・JSON・安全境界・runtime 同梱
                         ↓
みくくが具体設計と製造を進める
```

- 技術詳細を意識しない ≠ 技術判断が消えた
- 以前の判断が、必要なときに型として働く

## グラレコ構図案

- 左: 人が示す大きな方向の矢印
- 中央: 過去の型が入った知識レイヤー
- 右: 具体設計へ展開するカードとみくく
- みくくの表情・視線: 多数の技術カードを落ち着いて見渡す
- 吹き出し: 「技術判断は消えず、以前の型が働いていたのです…」

## 正確性メモ

- 記事にある技術判断だけを描く
- CLI のデフォルトは読み込み専用
- igapyon は Issue 登録時と最後のレビュー時に概要を認識

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
sections/005/graphic-recording.png
```
