# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: トークン単価と、仕事を終えるまでの費用は別
- section-text: sections/005/section-text.md
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

# トークン単価と、仕事を終えるまでの費用は別

## 主題

- トークン単価が下がっても、仕事を終えるまでの費用が同じ割合で下がるとは限らない。
- 入力・出力（推論トークンを含む）、キャッシュ、やり直し、ツール料金、待ち時間を含む。
- AutomationBenchのGPT-6 Luna `high` では前モデル比スコア+5.4ポイント、タスク費用−58%とOpenAIが発表。ただし特定ベンチマークの結果。

## 図解キーワード

- トークン単価
- 必要な品質
- 仕事完了までの費用
- 推論トークン
- やり直し
- ツール料金
- AutomationBench
- +5.4ポイント
- −58%

## 関係・流れ・対比

`入力 + 出力（推論含む） + キャッシュ + やり直し + ツール料金 + 時間 → 必要な品質で作業完了`

単価だけでなく、作業全体の費用で比較する。ベンチマーク値は普段の作業すべてに一般化しない。

## 図解構造

- layout-family: layers
- primary-relation: トークン単価だけではなく、品質を満たして作業を完了するまでの全要素を費用として見る

## グラレコ構図案

- 左: 小さな「トークン単価」ラベル。安い単価だけでは完了費用が決まらないことを示す。
- 中央: 入力・出力（推論含む）・キャッシュ・やり直し・ツール料金・時間を積み上げ、上端に「必要な品質で作業完了」と示す。
- 右: AutomationBenchの小さな評価カード「GPT-6 Luna high: +5.4ポイント / タスク費用 −58%」「特定ベンチマーク」。みくくは費用の積層図を説明する。
- みくくの表情・視線: 落ち着いて、全体費用の積み上げへ目線を向ける。
- 吹き出し: 「仕事を終えるまでの費用を比べたいです…！」

## 正確性メモ

- 推論トークンは課金対象の出力に含まれる。
- ツール料金は利用するツールによって別途発生する場合がある。
- +5.4ポイントと−58%はOpenAIが発表したAutomationBenchの値。
- ベンチマーク結果を普段の作業全般の保証として描かない。

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
sections/005/graphic-recording.png
```
