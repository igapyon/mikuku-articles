# Section Graphic Recording Image Prompt

## Source

- section: 000
- title: 開発日誌：プロンプトをレビューする Agent Skill をつくってみた。
- section-text: sections/000/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 開発日誌：プロンプトをレビューする Agent Skill をつくってみた。

## 主題

- プロンプトや Agent Skills の書き方への小さな不安から、レビュー用 Agent Skill を作り育てた開発日誌。
- GPT-5.5 Mediumで始め、GPT-5.6 Sol Ultraでレビューし、Terra Mediumで更新してv0.5.0へ運んだ。

## 図解キーワード

- 開発日誌
- プロンプトレビュー
- Agent Skill
- miku-prompt-lint
- GPT-5.5 Medium
- Sol Ultra
- Terra Medium
- v0.5.0

## 関係・流れ・対比

小さな不安 → レビュー観点 → miku-prompt-lint → 動作検証 → Sol Ultraレビュー → Terra Medium更新 → 人間確認 → v0.5.0

## グラレコ構図案

- 左: 「この書き方、いまも大丈夫？」という小さな不安とプロンプトの紙。
- 中央: miku-prompt-lintを中心に、GPT-5.5 Medium、Sol Ultra、Terra Mediumが役割を受け渡す流れ。
- 右: 人間の確認を経て到達するv0.5.0のリリース旗。
- みくくの表情・視線: 右側のv0.5.0を見ながら、少し緊張しつつ控えめに喜ぶ表情。
- 吹き出し: 「小さな不安から、ひとつのリリースへ」

## 正確性メモ

- GPT-5.5 Mediumは初期の観点整理とSkill作成、Sol Ultraは全体レビュー、Terra Mediumは更新を担当。
- 生成AIだけで判断を閉じず、人間が確認・採用・リリース判断を行う。

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
sections/000/graphic-recording.png
```
