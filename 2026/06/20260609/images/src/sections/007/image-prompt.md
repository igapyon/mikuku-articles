# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: 現代の言葉から 12 の原則を見直す
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# セクション別グラレコ制作用整理テキスト

## 主題

- 現代の開発実践を12原則から見直す
- 現代語は空から降ってきたものではなく、昔からの現場の悩みへの返事として見える

## 図解キーワード

- 現代実践への橋
- CI/CD
- 継続的デリバリー
- DevOps / BizDevOps
- バックログ見直し
- レトロスペクティブ
- 自己組織化チーム
- テスト自動化
- リファクタリング
- 小さく作って確かめる

## 対応の見取り図

| 現代の言葉 | つながる原則 |
|---|---|
| CI/CD | 短い間隔で届ける / 技術と設計 |
| 継続的デリバリー | 早く継続的に価値 |
| DevOps | 日々協力 / 動くもの中心 |
| バックログ見直し | 変化する要求 |
| レトロスペクティブ | ふりかえりと調整 |
| テスト自動化 | 技術的卓越性 |
| 小さく作る | 動くもの / シンプル |

## 構造

```text
12原則
  ↓
現代の言葉と重なる問題意識
  ↓
実践の意味が見えやすくなる
```

## 注意

- 公式対応表ではない
- 直接生まれたという意味でもない
- 入口に立つための見取り図

## みくく吹き出し案

- 「うぅ…現代の言葉も、昔からの悩みへの返事として見えるのです…」

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
