# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: 既存の TODO.md を壊さない
- section-text: sections/006/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 006 既存の TODO.md を壊さない

## 主題

- 既存 `TODO.md` を AI 都合で置き換えない
- 人間用メモやリリース作業を尊重する
- 必要なら専用セクションだけ足す

## 既存 TODO の用途

- 人間用の作業メモ
- リリース前の残作業
- 記事管理
- 画像回収の進捗
- 将来やりたい改善

## 追加する場所

```markdown
## AI Agent Current Tasks
```

## 図解

```text
既存 TODO.md
  ├─ 人間用メモ
  ├─ リリース作業
  └─ ## AI Agent Current Tasks
       ├─ current task
       ├─ blocker
       └─ retry log
```

## 中心メッセージ

- 人間が使っている棚を勝手に並べ替えない
- AI用の小さな引き出しだけ足す

## グラレコ構図

- 棚アイコンの一部に小さな引き出しを追加
- `TODO.md` を丸ごと上書きする矢印にはバツ印
- みくく: 「壊さず、足すだけにします…」

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
sections/006/graphic-recording.png
```
