# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: テーブル設計は古い地図になる
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# テーブル設計は古い地図になる

## 主題

DB を使う既存業務システムでは、テーブル設計が古い地図として効く。物理名と論理名の対応が、業務意味の理解を助ける。

## 見たい情報

- テーブル名
- カラム名
- 型 / 桁 / NULL / 主キー / インデックス
- テーブル論理名
- カラム論理名
- 項目説明
- コード値の意味

## 図の流れ

```text
物理名だけ
  ↓ 読みにくい
論理名・項目説明
  ↓
業務上の意味
  ↓
ソースコード解析が進む
```

## 注意点

- DB コメントにあれば取得しやすい
- なければ定義書や項目定義書を探す
- 古くても現行スキーマと照合できる
- 多少ずれていても、ないより助かる

## 吹き出し案

「古い地図でも、業務意味を読む手がかりになります…」

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
