# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: これは「爆速ウォーターフォール」だった
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# これは「爆速ウォーターフォール」だった

## 主題

- 約15時間で、要求から Pull Request、記事まで工程が順番に下流へ進んだ
- 速くなったのは工程の消滅ではなく、成果物作成と受け渡し
- 一つの小さなウォーターフォールを完了し、知見を次へ活かす

## 図解キーワード

- 約15時間
- 人の関与 約2時間
- 順番どおり
- 爆速ウォーターフォール
- 工程は残る
- 成果物づくり
- 受け渡し
- 小さく完了
- 次へ活かす

## 関係・流れ・対比

```text
気づく → 要求 → 責務設計 → リポジトリ → 初期製造
      → Issues → 追加製造 → PR・マージ → 記事
```

```text
一回の小さな開発: 上流から下流へ
完了後の知見: 次の開発の上流へ
```

## グラレコ構図案

- 左: 7月22日朝の最初のコミット
- 中央: 長いが高速な工程ウォーターフォール
- 右: 7月23日未明の記事原稿と、次の小さな流れへ向く矢印
- みくくの表情・視線: 速い工程をぱたぱた追いかける表情
- 吹き出し: 「工程はそのまま、作る時間と渡す時間が速くなりました…！」

## 正確性メモ

- 約15時間、人の関与約2時間は概算
- 生成 AI の動作時間は人の約2時間に含まない
- 全体の骨格は反復中心ではなく、基本的に順番どおり下流へ進む

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
