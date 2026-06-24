# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: 前回は、3つの Markdown から始めた
- section-text: sections/002/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 002 前回は、3つの Markdown から始めた

## 主題

- 状態管理の最小構成
- 目的、現在地、判断理由を会話の外へ出す
- 特定ツールに閉じない Markdown 運用

## 3ファイルの役割

| ファイル | 役割 | アイコン |
| --- | --- | --- |
| `GOAL.md` | 何を達成したら終わりか | 旗 |
| `TODO.md` | いま何をしているか | 地図 |
| `DECISIONS.md` | なぜその判断にしたか | 分岐メモ |

## 図解キーワード

- 目的
- 現在地
- 判断理由
- 会話の外へ
- 人間もAIも読める Markdown

## 流れ

```text
会話の中だけ
  ↓
プロジェクト側の Markdown
  ↓
人間 / Codex / Claude Code / Copilot agent が読める
```

## グラレコ構図

- 3枚のファイルカードを並べる
- 会話吹き出しから Markdown 棚へ移す矢印
- みくく: 「まずは小さく外へ出すのです…」

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
