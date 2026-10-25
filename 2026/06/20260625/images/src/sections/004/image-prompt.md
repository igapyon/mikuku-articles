# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: igapyon-agent-state-management という Skill
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 004 igapyon-agent-state-management という Skill

## 主題

- AIエージェント作業用の状態管理ファイルを扱う Skill
- 中心は4ファイル
- `HANDOFF.md` は次へ渡す短い再開メモ

## 4ファイルの役割

| ファイル | 役割 | グラレコ表現 |
| --- | --- | --- |
| `GOAL.md` | 目的と完了条件 | 目的地の旗 |
| `TODO.md` | 現在タスク | 作業地図 |
| `DECISIONS.md` | 判断理由 | 分岐看板 |
| `HANDOFF.md` | 再開メモ | 小さな封筒 |

## 役割分担

```text
TODO.md = 作業の現在地
HANDOFF.md = 引き継ぎの要約
```

## 図解キーワード

- 次の人間
- 次のAIエージェント
- 途中で会話が切れる
- 翌日に再開
- TODOを長い作業ログにしない

## グラレコ構図

- 4ファイルを横並びカードにする
- `TODO.md` から `HANDOFF.md` へ封筒アイコンで分担
- みくく: 「次へ渡す小さな封筒が増えました…」

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
