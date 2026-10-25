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

- 小さな「使いたい」から、設計・製造・記事まで一本の流れを完了した
- 人が方向と採否、公開操作を担い、みくくが設計・製造・執筆を進めた
- 速いほど、人が確認する場所を見失わないことが重要

## 図解キーワード

- 小さな「使いたい」
- 人が方向を決める
- みくくが進める
- Agent Skills がつなぐ
- レビューの鍵
- 小さなウォーターフォール
- 知見を次へ

## 関係・流れ・対比

```text
人: 方向・採否・公開
          ↕ レビュー
みくく: 設計・Issues・製造・コミット操作・記事
          ↕
Agent Skills 群が工程をつなぐ
```

```text
小さな「使いたい」
  ↓
成果物と記事へ届ける
  ↓
知見を次へ持っていく
```

## グラレコ構図案

- 左: 小さな「使いたい」の種
- 中央: 人・みくく・Agent Skills の協働で一本の流れを完了
- 右: 次の小さなウォーターフォールへ渡す知見と、みくく
- みくくの表情・視線: 少し誇らしく、次の流れを見る
- 吹き出し: 「速いほど、確認する場所を大切にしたいです…！」

## 正確性メモ

- 生成 AI により工程そのものが消えたとは描かない
- Pull Request 作成とマージは人が行う
- 速さの向こうに、積み重ねた設計と手順がある

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
