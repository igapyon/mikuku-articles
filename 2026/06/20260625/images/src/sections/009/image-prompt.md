# Section Graphic Recording Image Prompt

## Source

- section: 009
- title: この記事で使うなら
- section-text: sections/009/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 009 この記事で使うなら

## 主題

- 実際の使い方のイメージ
- 記事フォルダで Codex を起動
- グラレコ、状態管理、Note 公開前チェックへつなげる

## 使い方の流れ

```text
Download に記事用フォルダ
  ↓
記事 Markdown を置く
  ↓
Codex で開く
  ↓
グラレコ画像を作る
  ↓
igapyon-agent-state-management で作業状態を整理
  ↓
Note 掲載前チェックへ
```

## 短い頼み方

- `xxxx.md ファイルのグラレコ画像が欲しい`
- `igapyon goal`
- `igapyon 作業再開`
- `igapyon 状態管理`

## 価値

- 毎回ぜんぶ説明しなくてよい
- どの状態管理ファイルを読むかを Skill が持つ
- `TODO.md` を上書きしない方針も Skill が持つ
- 短いプロンプトで作業に戻れる

## グラレコ構図

- 記事フォルダから Codex へ
- グラレコ画像、状態管理ファイル、Note 公開チェックが並ぶ
- みくく: 「短い指示で作業に戻れるのが分かりやすいです…」

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
