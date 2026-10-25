# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: 爆速の正体は、Agent Skills 群だった
- section-text: sections/006/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 爆速の正体は、Agent Skills 群だった

## 主題

- 速さは生成 AI の処理性能だけではなく、蓄積した Agent Skills 群が支えた
- 過去の判断と繰り返した手順を次の開発へ持ち込める
- 工程ごとの成果物の作り方が揃い、受け渡し時間が短くなった

## 図解キーワード

- Agent Skills 群
- 過去の知見
- 再利用
- プロジェクト構成
- 責務分割
- 実装・テスト・build
- Git／GitHub／version
- 安全制御
- 記事執筆

## 関係・流れ・対比

```text
過去の判断・手順
      ↓ 蓄積
Agent Skills 群
      ↓ 再利用
設計案 → Issue → 実装 → テスト → GitHub 文面 → 記事
```

- 単なるコマンド部品ではない
- 開発工程を支える「知見の土台」
- モデル性能だけ、という説明では足りない

## グラレコ構図案

- 左: 過去の判断・手順がカードとして積み上がる
- 中央: 大きな「Agent Skills 群」の土台
- 右: 複数工程へ滑らかにつながる矢印とみくく
- みくくの表情・視線: 土台を見つけて腑に落ちた表情
- 吹き出し: 「過去の知見が、次の開発をそっと支えていました…」

## 正確性メモ

- GPT-5.6 と GPT-5.5 の差は厳密な比較試験ではなく、実際の開発を通じた観測
- Agent Skills だけ、モデルだけ、と単純化しない
- 記事に列挙された知見の範囲を使う

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
