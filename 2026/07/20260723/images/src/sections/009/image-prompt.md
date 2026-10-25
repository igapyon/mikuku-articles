# Section Graphic Recording Image Prompt

## Source

- section: 009
- title: おわりに
- section-text: sections/009/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# おわりに

## 主題

- 公開 MCP 実装から Node Core／CLI と Agent Skill へ橋を架けたベータ版
- CLI で動くだけでは、満足いく Agent Skill には足りない
- 発火、対象、承認、認証、診断まで境界を書くことで小さな道具になる

## 図解キーワード

- 公開 MCP 実装
- Node Core／CLI
- Agent Skill
- 動くだけでは足りない
- 発火
- 対象
- 人の承認
- 認証／診断
- 便利さと慎重さ
- 細い橋

## 関係・流れ・対比

```text
公開 MCP Server
  ↓ 入口を借りる
Node Core／CLI
  ↓ 作業の境界を書く
Agent Skill
  ↓
便利さ ＋ 慎重さ
```

## グラレコ構図案

- 左: Nulab さんの公開 MCP Server の入口
- 中央: Node Core／CLI から Agent Skill へ伸びる細い橋
- 右: 発火・対象・承認・認証・診断の五つの境界標識とみくく
- みくくの表情・視線: 少し緊張しながらも嬉しそうに橋を見る
- 吹き出し: 「動くだけでは、まだ足りなかったのです」

## 正確性メモ

- `backlog-api` と Agent Skill は MIT のベータ版
- Nulab 公式 MCP Server そのものではない
- 完成や十分な検証を断定せず、まだ確かめる点がある細い橋として描く

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
sections/009/graphic-recording.png
```
