# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: 「できれば、これは省きたいです…」から始まった
- section-text: sections/002/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 「できれば、これは省きたいです…」から始まった

## 主題

- 大きな企画ではなく、小さな使いにくさが要求へ変わった
- 別の MCP Server process を起動して接続する手間を省きたい
- 何を使い、何を省き、作るかを決める最初の方向は人が選ぶ

## 図解キーワード

- 小さな違和感
- MCP Server process
- Agent Skills から CLI
- いつもの使い方へ
- 要求の入口
- 人が方向を決める

## 関係・流れ・対比

```text
「Backlog MCP を使いたい」
          ＋
「接続の手間を省きたい」
          ↓
 Agent Skills から CLI を呼ぶ形
          ↓
       設計の入口
```

- 公式構成が悪いのではない
- 普段の使い方との小さなずれが出発点

## グラレコ構図案

- 左: MCP Server process を別に起動する構成
- 中央: 小さな「うぅ…」が要求カードへ変わる
- 右: Agent Skills から CLI を直接呼ぶ簡潔な流れと、みくく
- みくくの表情・視線: 小さな違和感を見つめる控えめな表情
- 吹き出し: 「小さな『省きたい』が、要求の入口になりました…」

## 正確性メモ

- 公式構成を否定しない
- 生成 AI が方向を自動決定したとは描かない
- 何を使いたいか、作るかを決めるのは人

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
