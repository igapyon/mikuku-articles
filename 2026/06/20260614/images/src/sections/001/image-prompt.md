# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# はじめに

## 主題

設計書ゼロの既存システムを、生成AIでいきなり完成設計書にするのではなく、ソフトウェア考古学のように痕跡から仕様メモを育てる。

## 図解キーワード

- 設計書ゼロ
- 既存システム
- ソースコードは事実を持つ
- 業務上の意味は別に探す
- 痕跡を拾う
- 仕様メモへ蒸留

## 流れ

```text
ソースコード / DB / 設定 / ログ
+ Excel / 運用メモ / 人の記憶
  ↓
仮説
  ↓
有識者レビュー
  ↓
使える仕様メモ
```

## 対比

| 単純な自動生成 | ソフトウェア考古学 |
| --- | --- |
| コードをそのまま文書化 | 痕跡を読み解く |
| 説明文は作れる | 理解の順番を作る |
| 業務意味が抜ける | 人の知識で照合する |

## 吹き出し案

「あ、あの…まずは痕跡を拾うところから始めます…」

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
sections/001/graphic-recording.png
```
