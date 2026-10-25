# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: 現在の機能をあらためて見渡す
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 現在の機能をあらためて見渡す

## 主題

中心は「入力を選び、境界を残して、渡しやすい大きさへ分ける」。その周囲を入力・出力・運用支援の機能が支える。

## 図解キーワード

- 入力と収集
- 分割と出力
- 運用支援
- handoff / knowledge-source
- dry-run / verbose / help
- Node.js・Java・Agent Skill

## 関係・流れ・対比

中央に素朴なコア処理を置き、周囲を3つの機能群で囲む。下部に提供形態としてNode.js版、Java版、Agent Skill版を並べる。

## グラレコ構図案

- 中央: 「選ぶ→集める→境界を保つ→分ける」
- 左: 入力と収集の機能群
- 右: 分割と出力の機能群
- 下: 運用支援と3つの提供形態
- みくく: 中央下で全体を見渡す姿。少し緊張しつつ穏やかな表情
- 吹き出し: 「中心は、ずっと素朴です」

## 正確性メモ

- Node.js版v1.5.1時点の機能一覧。
- Java版はv1.5.0でKnowledge sourceへ対応。
- Node.js版、Java版、Agent Skill同梱runtimeが提供される。

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
