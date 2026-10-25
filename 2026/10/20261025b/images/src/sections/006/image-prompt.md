# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: おわりに
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

# 終わったあとにも、続きがある

## 主題

- 処理を途中でやめたあとにも、後片づけが続き、次のリクエストが来る。
- 作りかけのデータと古い参照がどうなるかまで含めて、安全に終わらせる必要がある。
- 対応に力を尽くした人たちへ、ひと息つける時間が戻ることを願う。

## 図解キーワード

- 処理を途中でやめる
- 後片づけ
- 次のリクエスト
- 作りかけのデータ
- 古い参照
- 安全に終わらせる
- ひと息つけますように

## 関係・流れ・対比

```text
処理を途中でやめる → 後片づけ → 次のリクエスト
                       ├ 作りかけのデータは？
                       └ 古い参照を残していない？
後片づけの順番が、次の処理の安全につながる
```

## 図解構造

- layout-family: flow
- primary-relation: 終わったあとの後片づけが、次の処理の安全につながる

## 役割分担・判断軸

- 技術的な締め: 後片づけと次の処理の関係を振り返る。
- みくくの言葉: 対応にあたった人たちへの気遣いを短い吹き出しにする。
- 実際の作業者の姿、勤務時間、現場の状況や影響の規模は作らない。

## グラレコ構図案

- 左: 「処理を途中でやめる」の短い箱。続く矢印は途切れず、後片づけへ向かう。
- 中央: 最大の主図は「処理を途中でやめる」→「後片づけ」→「次のリクエスト」の落ち着いた3段階フロー。後片づけの下に小さな2つの確認枠「作りかけのデータは？」「古い参照を残していない？」。下端の一文「後片づけの順番が、次の処理の安全につながる」。
- 右: 右下のみくくと、対応にあたった人たちをねぎらう短い吹き出し。人物の群像、休憩室、カップ、花などの新しい場面や小道具を足さない。
- 最も大きく見せる主図: 後片づけから次の処理まで続く流れ。題名は「終わったあとにも、続きがある」。
- みくくの表情・視線: 右下に約20%の大きさで1人、少し安堵したやさしい表情で図から読者へ視線を向ける。同じ長い茶色のツインテール、黒と深紅のリボン、茶色の瞳、白い襟付きブラウス。物を持たず、手は下端に自然に置く。
- 吹き出し: あの…対応されたみなさまが、ひと息つけますように。

## 正確性メモ

- 結びにある内容だけを図と願いの言葉にする。新しい原因、CVE番号、修正の技術詳細は足さない。
- 願いを、実際に対応が完了した、全員が休めた、という事実の描写に変えない。
- 不具合への対応について述べており、弔意や死別の場面として描かない。
- 画像に設計文や正確性メモを印刷しない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右、主図を最大化。均一に明るい白〜薄いアイボリー。
- fully opaque background; no transparent or semi-transparent pixels
- 濃色の読みやすい文字、やわらかい手描き線、淡いオレンジ・ティール・緑の囲み。暗い陰影なし。
- 同じみくくを1人、短い吹き出し1つ、物を持たない。

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
- みくくは画面の15〜25%を占める説明役として描き、短い吹き出しを含める。固定条件を変更する場合は deviation に理由を書く
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
