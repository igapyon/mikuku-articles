# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: 帳票は埋もれやすい遺物かもしれない
- section-text: sections/005/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 帳票は埋もれやすい遺物かもしれない

## 主題

帳票はコード上の帳票テンプレートだけでは見つからない。業務上の帳票と実装上の形がずれることがある。

## 見つけにくい例

- Web 画面を PDF 出力する
- CSV を Excel に取り込んで加工する
- 画面を Excel に貼り付ける運用
- 実装上は別物だが業務上は帳票

## 対比

| コード上の姿 | 業務上の姿 |
| --- | --- |
| テンプレートがある | 帳票として扱う |
| CSV 出力 | Excel 加工後に帳票 |
| 画面表示 | PDF や貼り付けで帳票 |

## 注意点

- 「コードにないから存在しない」と言い切らない
- AI agent の仮一覧を有識者レビューで近づける
- 画面、バッチにも同じズレがあり得る

## 吹き出し案

「帳票は、思ったより深いところに埋もれているかもしれません…」

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
