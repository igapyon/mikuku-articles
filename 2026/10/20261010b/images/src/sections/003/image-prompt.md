# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: GPT-6.1 Solは、キャッシュ入力と処理区分にも注目
- section-text: sections/003/section-text.md
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

# GPT-6.1 Solは、キャッシュ入力と処理区分にも注目

## 主題

- GPT-6 SolとGPT-6.1 Solは通常入力 / 出力の標準単価が同じだが、キャッシュ入力は異なる。
- GPT-6.1 Solは処理区分により料金が変わり、UltrafastはStandardの6倍。
- 入力272Kトークン超では、リクエスト全体に長いコンテキスト料金が適用される。
- ここで示すのはAPI価格表の処理区分であり、Codex画面の選択肢とは別の情報。

## 図解キーワード

- GPT-6 Sol
- GPT-6.1 Sol
- キャッシュ入力 $0.20 → $0.10
- Batch / Flex
- Fast
- Ultrafast 6倍
- API料金
- Codex画面とは別
- 272Kトークン
- 長いコンテキスト

## 関係・流れ・対比

### キャッシュ

- キャッシュ入力: GPT-6 Sol $0.20 → GPT-6.1 Sol $0.10
- キャッシュ書き込み: どちらも $2.50

### GPT-6.1 Sol API料金の処理区分（入力 / キャッシュ入力 / 書き込み / 出力）

| 区分 | 価格 |
| --- | --- |
| Standard | $2 / $0.10 / $2.50 / $10 |
| Batch / Flex | $1 / $0.05 / $1.25 / $5 |
| Fast | $4 / $0.20 / $5 / $20 |
| Ultrafast | $12 / $0.60 / $15 / $60 |

`入力272Kトークン超 → 超過分だけでなくリクエスト全体に長文脈料金。GPT-6.1 Solは入力・キャッシュ関連2倍、出力1.5倍。`

## 図解構造

- layout-family: comparison
- primary-relation: 同じGPT-6.1 Solでも処理区分とコンテキスト長によって料金が変わる

## グラレコ構図案

- 左: GPT-6 Sol / GPT-6.1 Solのキャッシュ入力を「$0.20 → $0.10」で対比し、キャッシュ書き込みは「両方 $2.50」とする。
- 中央: 「GPT-6.1 SolのAPI料金」と明示し、Standard / Batch・Flex / Fast / Ultrafastの価格カードを配置。Codex画面の選択肢とは別のAPI価格区分だと注記し、Ultrafastに「Standardの6倍」を強調。
- 右: 272Kトークンの境界線を越えるとリクエスト全体へ長文脈料金が適用される図。みくくは中央の料金カードに目を向ける。
- みくくの表情・視線: 条件を丁寧に説明する落ち着いた表情。
- 吹き出し: 「モデル名だけでなく、処理区分もそろえたいです…！」

## 正確性メモ

- 処理区分別の価格はGPT-6.1 Solの短いコンテキストの料金。
- これはAPI価格表の処理区分。Codexの画面表示とは別の情報。
- Ultrafastの6倍はStandardとの比較。
- 272K超では入力・キャッシュ関連2倍、出力1.5倍。超過部分だけの加算ではない。
- 地域別処理の追加料金は価格カードに混ぜない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右の3領域、主図を最大化
- みくくは説明役として読める大きさで1人、短い吹き出しを1つ、物を持たない
- 背景は均一に明るい白〜ごく薄いアイボリーで全面不透明。濃色文字、淡い暖色の手描き線。

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
sections/003/graphic-recording.png
```
