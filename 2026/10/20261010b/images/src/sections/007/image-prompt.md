# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: おわりに
- section-text: sections/007/section-text.md
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

# おわりに

## 主題

- GPT-5.6からGPT-6へ、SolとLunaの単価はさらに下がった。
- GPT-6.1 SolにはUltrafastが加わり、速さと費用を処理区分ごとに見る。
- 現在の役割分担を小さな仕事で試し、品質・やり直し・全体費用を見ながら更新する。

## 図解キーワード

- GPT-5.6 → GPT-6
- GPT-6.1 Sol
- GPT-6 Luna
- Ultrafast
- Terraの後継掲載なし
- 小さな仕事
- 品質
- やり直し
- 作業全体の費用

## 関係・流れ・対比

`小さな仕事で試す → 品質・やり直し・作業全体の費用を見る → モデルの分担を更新`

現在の想定: `計画・難しい作業 → GPT-6.1 Sol xhigh` / `普段の実行 → GPT-6 Luna xhigh`。Terra自体はAPIモデルとして掲載中。

## 図解構造

- layout-family: cycle
- primary-relation: 小さな仕事で品質と費用を確かめ、モデルの役割分担を少しずつ描き直す

## グラレコ構図案

- 左: 「小さな仕事から試す」。GPT-5.6からGPT-6への価格変化を小さな下向き矢印で示す。
- 中央: 「計画・難しい作業 → Sol xhigh」「普段の実行 → Luna xhigh」の2枚の役割カード。
- 右: 品質・やり直し・全体費用を確かめて分担を更新する循環矢印。Terraは「後継掲載なし／現行API掲載中」と短く注記。みくくは循環の先を見る。
- みくくの表情・視線: 前向きだが慎重な表情。次の小さな検証へ目線を向ける。
- 吹き出し: 「数字と結果を見ながら、少しずつ試しますっ！」

## 正確性メモ

- GPT-5.6 TerraのAPI掲載とGPT-6系列の後継未掲載を区別する。
- 役割分担は「現在の想定」であり、確定した公式結論ではない。
- 記事本文にない日付・価格・モデル名を追加しない。

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
sections/007/graphic-recording.png
```
