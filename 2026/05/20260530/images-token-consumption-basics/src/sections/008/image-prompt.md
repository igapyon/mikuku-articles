# Section Graphic Recording Image Prompt

## Source

- section: 008
- title: なぜ料金や利用枠に関係するのか
- section-text: sections/008/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 008 なぜ料金や利用枠に関係するのか

## 主題

トークン数は、API の料金やサービスの利用枠に関係することがある。

## キーワード

- API
- 入力単価
- 出力単価
- 利用量
- 利用枠
- 上限
- 月額プラン

## 図解

```text
入力が大きい
  ↓
入力トークン増

出力が長い
  ↓
出力トークン増

トークン数
  ↓
料金・利用量・上限消費
```

## 対比

| 利用形態 | 見え方 |
| --- | --- |
| API | トークン数が料金に直結しやすい |
| Web UI | 個別の費用は見えにくいことがある |
| 月額プラン | 固定料金でも上限や利用枠がありうる |
| AI agent | 長い文脈で入力側が増えやすい |

## みくく吹き出し案

「見えにくくても、利用枠には関係していることがあるのです…」

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
sections/008/graphic-recording.png
```
