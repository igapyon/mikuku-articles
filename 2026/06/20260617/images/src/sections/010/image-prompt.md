# Section Graphic Recording Image Prompt

## Source

- section: 010
- title: 同じプロンプトをもう一度実行する
- section-text: sections/010/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 010 同じプロンプトをもう一度実行する

## 主題

- `index.json` と `SKILL.md` の追記後、同じプロンプトを再実行する
- ユーザー依頼は変えない
- Agent Skill 側の入口だけが変わる

## 観察された流れ

```text
SKILL.md
  ↓
README.md
  ↓
index.json
  ↓
候補 Markdown
  ↓
本文を読む
  ↓
Agent Skills の主張を整理
```

## 主な整理

- Agent Skills は単なるプロンプト集ではない
- AI agent に渡す再利用可能な作業仕様
- `SKILL.md` は入口、判断基準、参照先、出力形式を決める
- 詳細知識は `references/`、出力構造は `templates/`、温度感は `examples/`

## キーワード

- 同じプロンプト
- 入口の変化
- index.json を先に読む
- 本文 Markdown へ進む

## 吹き出し候補

「同じお願いでも、最初に見る場所が変わりました…」

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
