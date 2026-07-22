# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: Nulab 公式の Backlog MCP Server
- section-text: sections/002/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Nulab 公式の Backlog MCP Server

## 主題

- Nulab が 2025 年 5 月に公開した MIT ライセンスの MCP Server
- 多様な Backlog 情報を自然言語から扱える
- 公式公開でも保証・公式サポートはなく、権限確認と自己責任が必要

## 図解キーワード

- Backlog MCP Server
- GitHub 公開
- MIT
- stdio
- Streamable HTTP
- toolset／fields
- 読み取り／変更
- 自己責任

## 関係・流れ・対比

```text
AI agent → MCP Server → Backlog
                  ├ 読み取り
                  └ 作成・更新・削除
```

- 便利さ: project、issue、Wiki、document、Git、通知など
- 注意: 保証なし／公式サポートなし／内容と権限を確認

## グラレコ構図案

- 左: AI agent と Backlog をつなぐ MCP Server
- 中央: Docker／npx／Node.js、stdio／Streamable HTTP の入口カード
- 右: 読み取りと変更操作の分岐、注意ボックス、みくく
- みくくの表情・視線: 安心しすぎない慎重な表情で注意ボックスを見る
- 吹き出し: 「公式でも、権限の確認は大切です…」

## 正確性メモ

- 「公式」を保証や公式サポートがあるという意味にしない
- Docker 以外の起動方法も描く
- 対応対象をすべて長文で列挙せず、代表アイコンで示す

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
sections/002/graphic-recording.png
```
