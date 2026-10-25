# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# はじめに

## 主題

- Nulab さんの Backlog MCP Server を使ってみたい、という素朴な出発点
- 別 process の MCP Server を起動せず、Node Core／CLI と Agent Skill へ変換する発想
- MCP は「つなぐ」、Agent Skill は「どう扱うかを伝える」

## 図解キーワード

- 公式 MCP
- Docker／npx／Node.js
- 別 process
- MCP transport
- Node Core／CLI
- Agent Skill

## 関係・流れ・対比

```text
公式 MCP を使いたい
  ↓ でも別 process は起動したくない
公開 source code
  ↓ MCP transport を通さない形へ
Node Core／CLI ＋ Agent Skill
```

## グラレコ構図案

- 左: Docker／npx／Node.js から MCP Server を起動する入口
- 中央: 「別 process は起動したくない」という気づきと変換矢印
- 右: 「MCP＝つなぐ」「Agent Skill＝扱い方」の二枚カードとみくく
- みくくの表情・視線: 驚きと好奇心のある表情で中央の変換を見る
- 吹き出し: 「ちょっと Agent Skill にしてみたいな…！」

## 正確性メモ

- Docker だけでなく `npx` と Node.js の起動方法もある
- GPT-5.6 Sol Medium への驚きは本文にあるが、図の中心は変換の発想に置く
- MCP と Agent Skill は役割が少し違う、と表現する

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
sections/001/graphic-recording.png
```
