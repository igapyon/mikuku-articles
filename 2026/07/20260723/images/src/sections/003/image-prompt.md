# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: MCP を、そのまま包んだわけではありません
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# MCP を、そのまま包んだわけではありません

## 主題

- MCP Server への接続設定集ではなく、三層に責務を分けた派生プロジェクト
- 公開 handler の振る舞いを保ちつつ transport 境界を外す
- CLI 変換と Agent Skill の運用部分を分離する

## 図解キーワード

- 公開 tool handler
- MCP transport
- backlog-api
- Node Core／CLI
- backlog-api-skills
- SKILL.md
- 操作 map
- 安全規則

## 関係・流れ・対比

```text
Nulab Backlog MCP Server
  ↓ 公開 handler と API の振る舞い
backlog-api
  ↓ transport を外した Node Core／CLI
backlog-api-skills
  ↓ runtime ＋ 発火・確認・安全運用
Agent Skill
```

## グラレコ構図案

- 左: 上流の Nulab Backlog MCP Server
- 中央: 三層を縦に貫く変換フローを大きく描く
- 右: 「責務を混ぜない」「由来を追える」の二つの効果とみくく
- みくくの表情・視線: 落ち着いた表情で層の境界線を見る
- 吹き出し: 「内側の境界を、きちんと分けます…」

## 正確性メモ

- `backlog-api` と `backlog-api-skills` は非公式の派生プロジェクト
- `backlog-api` は MIT のベータ版で、interface や動作が変わる可能性がある
- Nulab 公式 MCP Server そのものとして描かない

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
