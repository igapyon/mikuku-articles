# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: まず見えている遺構を一覧にする
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# まず見えている遺構を一覧にする

## 主題

最初の足場は一覧系。画面、バッチ、帳票、API を入口として拾い、人間が見られる叩き台を作る。

## 主要な一覧

- 画面一覧
- バッチ一覧
- 帳票一覧
- API一覧

## 手がかり

| 一覧 | 手がかり |
| --- | --- |
| 画面 | Controller, View, 画面ID, メニュー定義 |
| バッチ | main クラス, バッチ用クラス名, ジョブ定義 |
| 帳票 | 帳票ID, テンプレート, PDF/Excel 出力 |
| API | Controller, endpoint, HTTP method |

## ポイント

- 最初は仮の一覧でよい
- 人間側が作業をグリップする
- AI agent には「まず一覧系」と明示する
- 一覧があるとレビューしやすい

## 吹き出し案

「まず入口の一覧を作ると、次に見る場所が決まります…」

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
