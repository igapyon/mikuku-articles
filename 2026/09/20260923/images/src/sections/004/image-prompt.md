# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: 試した結果を伝え、話をつなぐ
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Style Contract

- style-profile: mikuku-graphic-recording-v1
- horizontal 3:2 technical graphic-recording poster
- uniformly bright white to very pale ivory paper (e.g. #FFFDF5), subtle warm tint, soft hand-drawn lines, medium-high information density
- fully opaque background; no transparent or semi-transparent pixels; no alpha transparency; do not generate a transparent canvas; export an opaque image
- dark, high-contrast text including small annotations; pastel colors for accents, not faint lettering
- no dark vignette, muddy gray-brown cast, heavy aged-paper shading, or dark shadows behind text
- canonical character lighting must not darken the poster background
- use at least a left, center, and right region and make one article-grounded diagram the largest element
- keep Mikuku recognizable and large enough to read as the explaining character (roughly 15–25% of the canvas)
- include one short speech bubble based on the section summary or its `グラレコ構図案`
- do not add scenic background decoration that is not grounded in the section

## Section Summary

# 試した結果を伝え、話をつなぐ

## 主題

- 生成AIの提案を試したら、手元で起きた結果を言葉にして返す
- 何をしたか・何が起きたか・期待と何が違ったかを順序立てて伝える
- 起きた事実と推測を分け、回答の根拠も自分で確かめる

## 図解キーワード

- 提案
- 試す
- 実施結果
- 事実
- 推測
- 期待との差
- 根拠の確認
- 次の相談

## 関係・流れ・対比

- 提案 → 試す → 結果を観察 → 事実と推測を分けて報告 → 次の相談
- 回答の「確認済み」だけで終えず、出典や実際の結果と照合

## 図解構造

- layout-family: flow
- primary-relation: 提案を試し、結果を事実と推測に分けて伝えて次の相談につなぐ

## グラレコ構図案

- 左: 生成AIの提案を受け取り、A4に配置して印刷する
- 中央: 印刷結果「本文の文字が小さい」と、事実／推測を分ける二枚のカード
- 右: 「文章を短くしたい」という次の相談へ進む矢印。下部に出典・実際の結果との照合チェック
- みくくの表情・視線: 右下で納得した表情、結果カードから次の相談へ視線を向ける
- 吹き出し: 「試した結果を伝えます」

## 正確性メモ

- 記事本文に明記された事実だけを使う
- A4印刷の例は記事の例として描き、一般的な実験結果に見せない
- 事実と推測を区別し、生成AIの返答だけで根拠確認が完了するように描かない

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、主図を最大化
- みくくは説明役として読める大きさで1人、短い吹き出しを1つ、物を持たない

## 変更（deviation）

- none

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
- みくくを極端に小さくしたり、吹き出しを黙って削除したりしない。変更する場合は下の deviation に理由を書く
- 日本語ラベルは短く、少数に絞る
- 長文を画像内に入れすぎない
- 明るく清潔で、Note.com や技術記事に合うビジュアル
- 写実寄り、暗い色味、無機質な企業プレゼン風は避ける
- みくくに物を持たせない

## Image Text Policy

- 画像内テキストは section summary の語句を短く整理して使う
- 本文の長い文をそのまま入れない
- 文字が崩れても、元記事や section-text.md は変更しない

## Article-specific Design

- section-text.md の主題、関係、構図、短いラベルを保持する
- section-text.md の `layout-family` と `primary-relation` を別の図解形式へ変えない

## Deviation Record

- none

## Output Target

Save the generated image as:

```text
sections/004/graphic-recording.png
```
