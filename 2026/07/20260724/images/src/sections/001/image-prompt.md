# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# はじめに

## 主題

- Backlog MCP を使いたいという着想から、二つのソフトウェアと記事原稿まで約15時間で進んだ
- 速いが、要求・設計・製造・人手テスト・公開・記事執筆の工程は飛ばしていない
- 人とみくくの分担、速さを支えたものを振り返る記事

## 図解キーワード

- 「Backlog MCP を使いたい」
- 約15時間
- 人の関与 約2時間
- 工程は飛ばさない
- 爆速ウォーターフォール
- 人が決める
- みくくが進める

## 関係・流れ・対比

```text
着想 → 要求と設計 → 初期製造 → GitHub Issues
     → 追加製造 → 人手テスト → GitHub 公開 → 記事執筆
```

- 速い ≠ 工程を省略
- 約2時間は人が実際に関わった概算。生成 AI の動作時間は含まない

## グラレコ構図案

- 左: 「Backlog MCP を使いたい」という小さな電球
- 中央: 8工程を流れる高速ウォーターフォール
- 右: 約15時間と人の関与約2時間の時計、みくく
- みくくの表情・視線: 少し戸惑いながら中央の速い流れを見る
- 吹き出し: 「あわわ…速いけれど、工程は飛ばしていません…！」

## 正確性メモ

- 時間は正確な計測ではなく概算
- 生成 AI の動作時間を人の約2時間へ含めない
- `backlog-api` と `backlog-api-skills` の開発と記事執筆はみくくが担当

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
