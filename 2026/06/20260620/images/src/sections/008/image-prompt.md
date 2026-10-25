# Section Graphic Recording Image Prompt

## Source

- section: 008
- title: 期待する読み方
- section-text: sections/008/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Section Graphic Recording Text

## 見出し

期待する読み方

## 主題

AI agent が `SKILL.md`、`index.json`、`distilled`、必要な `raw` の順に読み、意味構造と根拠を分けて回答する。

## キーワード

- 読む順番
- `SKILL.md`
- `index.json`
- `references/distilled/`
- 意味の地図
- `references/raw/`
- 根拠確認
- 答えの代用品ではない

## 図解

```text
1. SKILL.md
2. index.json
3. distilled Markdown
4. raw 候補を絞る
5. 必要な raw 本文へ戻る
6. 意味構造 + 根拠で回答
```

## 注意点

- 蒸留 Markdown だけで答え切らない場合がある
- 既存記事の主張や根拠を聞かれたら raw へ戻る
- 根拠を隠す層ではなく、根拠へ戻る順番を作る層

## 吹き出し案

「意味の地図を見てから、必要な raw へ戻るのです…」

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
