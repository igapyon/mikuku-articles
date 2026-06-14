# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: 発掘した一覧を育てる
- section-text: sections/006/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 発掘した一覧を育てる

## 主題

一覧は最初に作って終わりではない。個別仕様を抽出するたびに一覧の解像度を上げる。

## 抽出する仕様

| 対象 | 仕様の例 |
| --- | --- |
| 画面 | 入力項目、表示項目、検索条件、検証、更新、遷移、権限 |
| バッチ | 起動条件、対象データ、処理内容、更新先、ログ、異常時 |
| 帳票 | 出力条件、出力項目、集計単位、並び順 |
| API | request, response, 認証、エラー、参照・更新対象 |

## 育つ流れ

```text
仮の一覧
  ↓
個別仕様を抽出
  ↓
一覧へ説明を追記
  ↓
実態に近い一覧
```

## 図解キーワード

- 仮の入口一覧
- 説明を書き足す
- 表の列が増える
- 仕様抽出で解像度が上がる

## 吹き出し案

「一覧は作って終わりではなく、育てるものなのです…」

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
sections/006/graphic-recording.png
```
