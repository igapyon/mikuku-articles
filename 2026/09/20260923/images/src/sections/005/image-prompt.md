# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: なぜ、小学校国語が生成AIとの会話のヒントになるのか
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

# なぜ、小学校国語が生成AIとの会話のヒントになるのか

## 主題

- 人間同士の「伝え合い」を手掛かりに、生成AIへの伝え方を組み立てられる場面がある
- 人間が書いた文章や会話データを学習・調整に使う例はあるが、モデルごとに方法は異なる
- 生成AIを人間と同じように理解する相手とみなすのではなく、会話の進め方を参考にする

## 図解キーワード

- 人間同士の伝え合い
- 背景
- 返答
- 補足
- 学習・調整の例
- モデルごとに異なる
- 会話のヒント
- 同じ理解ではない

## 関係・流れ・対比

- 人間同士: 背景を説明 → 返答を受ける → 必要なら補足
- 生成AIとの会話: 背景・条件を伝える → 回答を読む → 補足して次の回答の手掛かりを増やす
- 会話の進め方は参考にできる ≠ AIが人間と同じように理解している

## 図解構造

- layout-family: comparison
- primary-relation: 人間同士と生成AIとの会話を並べ、伝え方の参考になる点と同一視しない注意を示す

## グラレコ構図案

- 左: 人間同士の会話で「背景→返答→補足」と進む小さな図
- 中央: 二つのやりとりをつなぐ「伝え方のヒント」の橋。横に「モデルごとに学習方法は異なる」の注記
- 右: 生成AIとの「背景・条件→回答→補足」の図と、「人間と同じ理解ではない」の注意枠
- みくくの表情・視線: 右下で穏やかな説明顔、橋と注意枠の両方を見る
- 吹き出し: 「伝え方のヒントとして」

## 正確性メモ

- モデルごとに学習方法は異なり、人間が書いた文章や会話データを学習・調整に使う例がある、という限定を保つ
- 個別の資料の説明を全モデルへ一般化しない
- 生成AIを人間と同じように理解する存在として描かない

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
sections/005/graphic-recording.png
```
