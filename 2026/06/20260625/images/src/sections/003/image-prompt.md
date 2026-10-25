# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: まえやっていた手順を思い出すのが少し辛い
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 003 まえやっていた手順を思い出すのが少し辛い

## 主題

- 小さい構成でも、毎回の始め方に迷う
- 既存 `TODO.md` の扱いに迷う
- 作業再開メモは別に分けたくなる

## 図解キーワード

- 新しいリポジトリで何を頼む？
- 既存 `TODO.md` をどう扱う？
- 作業再開メモ
- 4つめのファイル
- 使い方を思い出す辛さを減らす

## 対比

```text
仕組みは小さい
でも
使い始めの手順は毎回迷う
```

## 流れ

```text
3ファイル構成
  ↓
運用時の迷い
  ↓
HANDOFF.md の必要性
  ↓
Agent Skill にまとめる
```

## グラレコ構図

- 左: 3ファイルを前に迷う小さなメモ
- 中央: 「どう頼むんだっけ？」の雲
- 右: `HANDOFF.md` が追加される
- みくく: 「仕組みの使い方も、Skill に置きたいのです…」

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
