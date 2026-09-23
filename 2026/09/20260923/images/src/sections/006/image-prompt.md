# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: 学校における生成AIの取り組み
- section-text: sections/006/section-text.md
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

# 学校における生成AIの取り組み

## 主題

- 文部科学省のガイドラインは、児童生徒が生成AIとの上手な会話の進め方を学ぶ場面を挙げている
- 小学校段階での直接利用は、発達段階などを踏まえ慎重な判断が必要
- 実践事例には、生成AIへの音声入力や、動画を使う授業で生成AIの助言を活用する例がある

## 図解キーワード

- 学校
- 上手な会話
- 学ぶ場面
- 小学校段階
- 慎重な判断
- 音声入力
- 動画を使った授業
- 生成AIの助言

## 関係・流れ・対比

- 学校で学ぶ場面: 生成AIとの上手な会話
- 小学校段階の直接利用: 発達段階などを踏まえて慎重に判断
- 実践事例: 音声入力／動画を使った授業で生成AIの助言を活用

## 図解構造

- layout-family: cards
- primary-relation: 学校での学び・慎重な判断・実践事例を3つのカードで整理する

## グラレコ構図案

- 左: ガイドラインのカード「上手な会話を学ぶ」
- 中央: 小学校段階での直接利用について「発達段階などを踏まえ慎重に判断」の目立つ注意カード
- 右: 2つの実践例カード「音声入力」「動画を使った授業＋生成AIの助言」
- みくくの表情・視線: 右下で希望を感じる穏やかな表情、事例から中央の注意へ視線を向ける
- 吹き出し: 「方法は広がりそうです」

## 正確性メモ

- 記事本文に明記された事実だけを使う
- 音声入力は生成AIへの入力例として示す
- 動画を使った授業の事例は、生成AI自身が動画を入力・解析した例とは限らないため、そのように描かない
- 小学校段階での直接利用には慎重な判断が必要という但し書きを省かない

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
sections/006/graphic-recording.png
```
