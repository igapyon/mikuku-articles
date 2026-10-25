# Section Graphic Recording Image Prompt

## Source

- section: 008
- title: Agent Skill にしたことで、運用が会話から少し離れた
- section-text: sections/008/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 008 Agent Skill にしたことで、運用が会話から少し離れた

## 主題

- 長い初期プロンプトを毎回会話に貼らない
- 運用ルールを Skill 側へ置く
- `SKILL.md` を入口にして必要資料を読む

## 構造

```text
短い依頼
  ↓
SKILL.md
  ↓
references/
  ↓
templates/
  ↓
安定した運用
```

## Context Engineering

- プロンプトを毎回よくするだけではない
- 作業時に参照できる場所へ判断材料を置く
- プロンプトの外に足場を置く

## 対比

| 以前 | Skill化後 |
| --- | --- |
| 会話に長い運用プロンプト | Skill 側に運用ルール |
| 毎回貼る | 必要に応じて読む |
| 手順が揺れる | 参照場所が安定 |

## グラレコ構図

- 会話吹き出しから `SKILL.md` の入口へ移る
- `references/` と `templates/` が本棚として描かれる
- みくく: 「プロンプトの外に足場を置く感じです…」

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
