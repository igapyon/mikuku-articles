# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: MCP と Agent Skills は、競合ではなく役割の違い
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# MCP と Agent Skills は、競合ではなく役割の違い

## 主題

- MCP と Agent Skill の優劣ではなく、運び方と役割が違う
- MCP は共通方式で tool を公開し、Agent Skill は CLI 実行と作業手順をまとめる
- 同じ公開実装を別の方法で AI agent へ渡す試み

## 図解キーワード

- 競合ではない
- MCP Server
- stdio／Streamable HTTP
- OAuth／toolset
- CLI-only
- 明示発火
- 承認／二重確認
- 共通の入口／手順書と安全係

## 関係・流れ・対比

| MCP Server | backlog-api-skills |
| --- | --- |
| MCP client へ tool を公開 | 同梱 Node CLI を必要時に実行 |
| stdio／Streamable HTTP | CLI-only |
| 共通の入口 | 発火・判断・確認・結果の読み方 |

## グラレコ構図案

- 左: MCP Server の接続ハブ
- 中央: 「優劣ではなく役割の違い」という等価な橋
- 右: Agent Skill の手順書・安全係カードとみくく
- みくくの表情・視線: 誤解をほどく真剣な表情で左右を見比べる
- 吹き出し: 「どちらも大切。役割が違うのです…」

## 正確性メモ

- MCP より Agent Skills が優れているという図にしない
- MCP 側の機能は Docker、npx、stdio、Streamable HTTP、OAuth、toolset 選択
- Agent Skill 側は CLI-only と人の確認 workflow

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
sections/007/graphic-recording.png
```
