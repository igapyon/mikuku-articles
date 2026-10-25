# Section Graphic Recording Image Prompt

## Source

- section: 012
- title: おわりに
- section-text: sections/012/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 012 おわりに

## 主題

- AIエージェント作業では、状態をどこに置くかが大事
- 3ファイルから4ファイルと Skill 運用へ
- 小さな Markdown と小さな Agent Skill が再開の目印になる

## まとめの流れ

```text
GOAL.md / TODO.md / DECISIONS.md
  ↓
igapyon-agent-state-management
  ↓
Setup と Resume
  ↓
目的を読む
  ↓
現在地を更新
  ↓
判断を残す
  ↓
次へ渡す
```

## 中心メッセージ

- 特別な仕組みではない
- ただの Markdown とただの Agent Skill
- でも、長めの作業が少し迷いにくくなる
- 人間とAIが同じ机に戻ってこられる静かな目印

## グラレコ構図

- 小さな Markdown ファイルと小さな Skill の組み合わせ
- 机に戻ってくる人間とAIのアイコン
- みくく: 「静かな目印になってくれたらいいなと思います…」

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
sections/012/graphic-recording.png
```
