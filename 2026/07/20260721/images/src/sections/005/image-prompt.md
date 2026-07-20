# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: 二段階で準備する
- section-text: sections/005/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 二段階で準備する

## 主題

- 第1段階で配備先と入力範囲を確認し、`manual-input/` を用意して停止する。
- 人が資料を追加するか、追加なしと確認してから第2段階へ進む。
- 人が丁寧に準備した資料と、多数の Markdown を自動でまとめた資料を両立させる。

## 図解キーワード

- 第1段階
- manual-input/
- 人の確認
- 第2段階
- upload/
- 自動と手動の両立

## 関係・流れ・対比

第1段階「対象を確認」 → 待ち合わせ「資料追加／追加なし」 → 第2段階「配備用に整える」

手作り資料 ＋ 自動バンドル資料 → 最終的な upload/

## グラレコ構図案

- 左: 第1段階の入力範囲確認と `manual-input/`。
- 中央: 「ここで停止」と人の確認を示す待ち合わせ地点。
- 右: 第2段階のバンドル・変換と `upload/`。
- みくくの表情・視線: 中央の待ち合わせ地点を安心させるように見守る。
- 吹き出し: 「ここで、人の資料を待ちます」

## 正確性メモ

- 原本と元フォルダは変更しない。
- 人の確認なしに最初から最後まで自動実行する図にしない。

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
