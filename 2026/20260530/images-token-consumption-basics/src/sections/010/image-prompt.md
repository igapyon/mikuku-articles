# Section Graphic Recording Image Prompt

## Source

- section: 010
- title: いまのところの整理
- section-text: sections/010/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 010 いまのところの整理

## 主題

トークン、入力/出力、コンテキスト、AI agent、料金や利用枠の関係をまとめる。

## まとめキーワード

- 生成AIはトークンをもとに文章を扱う
- トークンは小さな部品
- 文字数と完全一致しない
- 入力トークンと出力トークンがある
- コンテキストウィンドウには限りがある
- AI agent は全部を常時見ていない
- compaction は完全保存ではない
- API料金や利用枠に関係しうる

## 総まとめ図

```text
文章・履歴・資料
  ↓
入力トークン
  ↓
コンテキストウィンドウ内で処理
  ↓
出力トークン
  ↓
回答
  ↓
利用量・料金・上限に関係
```

## 読者に残したい見方

- 短い質問の裏側に長い履歴があること
- 添付ファイルも入力に関係すること
- 文脈には限りがあること
- 必要な文脈だけを持ち込むこと

## みくく吹き出し案

「トークンのことが少しわかると、生成AIの見え方が変わるのです…」

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
sections/010/graphic-recording.png
```
