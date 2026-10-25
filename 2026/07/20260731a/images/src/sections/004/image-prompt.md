# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: Agent Skill は薄く、文字コード処理は CLI へ
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Agent Skill は薄く、文字コード処理は CLI へ

## 主題

- Skill は「いつ・どの操作・どの範囲」を判断する薄い入口
- 文字コードや revision、atomic mutation などの繊細な処理は CLI runtime が担当
- 制御用 request は UTF-8 JSON、対象ファイルの表現だけを CLI に任せる

## 図解キーワード

- Agent Skill
- CLI runtime
- 役割分担
- UTF-8 JSON
- 対象ファイル
- 繊細な境界

## 関係・流れ・対比

| Agent Skill | CLI runtime |
| --- | --- |
| 発火・操作・範囲 | encoding・rule・revision |
| 読む範囲 | patch・atomic mutation |
| 固定 launcher | diagnostics |

## グラレコ構図案

- 左: AI agent の依頼
- 中央: 薄い Agent Skill と厚い CLI runtime の二層
- 右: Windows-31J の対象ファイル
- みくくの表情・視線: 二層の境界をやさしく見る
- 吹き出し: 「繊細な処理は CLI に任せるのです…」

## 正確性メモ

- 制御経路は UTF-8 JSON
- Skill 自身へ文字コード処理を実装していない

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
