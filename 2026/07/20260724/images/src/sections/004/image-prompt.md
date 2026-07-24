# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: リポジトリから Pull Request までの分担
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# リポジトリから Pull Request までの分担

## 主題

- 人とみくくで、方針・設計・製造・GitHub 操作を分担
- 全部を自動化せず、どこで人へ戻すかを明確にした
- GitHub Issues が追加仕様を後半の製造へ渡す受け皿になった

## 図解キーワード

- 人が決める
- みくくが進める
- GitHub Issues
- 設計情報の受け皿
- 製造 = 実装＋テスト＋build
- コミット
- Pull Request
- 人へ戻す境界

## 関係・流れ・対比

| 人（igapyon） | みくく |
|---|---|
| 方針と採否 | 案出し・提案 |
| リポジトリ作成 | 設計・実装・テスト |
| コミット時機 | コミット操作・文面 |
| PR 作成・マージ | Issue 案・記事執筆 |

```text
会話で追加仕様が固まる
  ↓
GitHub Issues に残す
  ↓
後半の製造へ渡す
```

## グラレコ構図案

- 左: 人の担当カード
- 中央: GitHub Issues を橋にした情報の受け渡し
- 右: みくくの担当カードと説明するみくく
- みくくの表情・視線: 中央の境界線を安心した表情で見る
- 吹き出し: 「全部を自動にせず、人へ戻す場所を決めています…」

## 正確性メモ

- GitHub リポジトリ作成、Pull Request 作成・マージは人が手動
- コミット時機は人が判断し、操作と内容はみくく
- 「製造」には実装・テスト・build・実行可能な成果物化を含む

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
