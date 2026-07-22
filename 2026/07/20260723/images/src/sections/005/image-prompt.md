# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: Agent Skill として、安全確認を前へ置く
- section-text: sections/005/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Agent Skill として、安全確認を前へ置く

## 主題

- 読み取りは既定で許可、作成・更新・削除は直前の人の承認が必要
- 破壊的・広範囲な操作は二段階目の確認を行う
- 認証情報と診断情報を限定して扱う

## 図解キーワード

- READ
- CREATE／UPDATE／DELETE
- 人の直前承認
- `--allow`
- 影響確認
- `--confirm-destructive`
- 環境変数
- safe diagnostics

## 関係・流れ・対比

```text
READ → 既定で許可

CREATE／UPDATE／DELETE
  ↓ 対象・operation・変更内容を提示
人の直前承認
  ↓ --allow
破壊的・広範囲？ ─ yes → 影響を再確認 → --confirm-destructive
```

## グラレコ構図案

- 左: READ と WRITE の分岐
- 中央: 承認から `--allow`、再確認への安全ゲートを大きく描く
- 右: API key は環境変数、診断は限定情報だけ、という盾カードとみくく
- みくくの表情・視線: 慎重な表情で中央の停止線を見る
- 吹き出し: 「進み方と、立ち止まる場所を決めます…」

## 正確性メモ

- 一度の承認で破壊的操作まで同時承認しない
- API key を会話へ貼る運用にしない
- `--verbose` でも本文、検索語、個人情報、error body、認証情報を出さない設計

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
sections/005/graphic-recording.png
```
