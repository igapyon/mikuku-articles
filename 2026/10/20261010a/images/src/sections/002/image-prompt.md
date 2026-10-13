## Edit Request

Use the supplied image as the edit target, not merely a style reference. Preserve the existing layout, Japanese text, Mikuku face, hair, clothing, pose and speech bubble. Change the workflow illustrations to show an AI agent actively performing the tasks described below. Keep the same 3:2 canvas. Existing text remains verbatim except the added short AI role labels. Do not redraw or redesign Mikuku. Do not let Mikuku hold any objects.

# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: ドキュメントが実務の中で活きる
- section-text: sections/002/section-text.md
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

# ドキュメントが実務の中で活きる

## 主題
- 依頼に合わせてAIエージェントが文書を参照し、確認と根拠を添えた指摘を進める。
- 編集できる環境・変更の許可・判断材料の3条件がそろう場合に修正。
- 見逃しを減らす助けになり、担当者間で判断の観点を共有できる。

## 図解キーワード
依頼 / 文書を参照 / AIエージェント / 確認 / 根拠と一緒に指摘 / 修正の条件 / 見逃しを減らす / 判断の観点を共有

## 関係・流れ・対比
人の依頼 → AIエージェントが文書を参照 → 確認 → 根拠と一緒に指摘
編集できる環境 ＋ 変更の許可 ＋ 判断材料がそろう → 条件がそろえばAIエージェントが修正

## 図解構造
- layout-family: flow
- primary-relation: AIエージェントが文書に沿って確認し、条件付きで修正する実務の流れ。

## グラレコ構図案
- 編集対象: 既存 images/002.png。既存の構図と情報を保つ。
- 左: 依頼と文書参照。文書参照に小さなAIエージェントが実際に文書を読む描写。
- 中央: 「確認」の紙と虫眼鏡を、同じAIエージェントが虫眼鏡で文書を点検する姿に置き換える。ラベル「AIエージェント」を明瞭に付ける。チェック印と根拠箇所のハイライトで、作業中だと示す。右隣の根拠付き指摘はAIがチェック済み結果を返している様子。
- 下: 3条件を完全に保持。その先の修正カードは同じAIエージェントが文書を修正する動作を追加。条件なしの修正に見せない。
- 右: 既存2つの効果とみくくを保持。
- みくくの表情・視線: 元画像と同じキャラクター、説明する表情・ポーズをそのまま保持。
- 吹き出し: 「あの…根拠と条件も、一緒に確認しますね。」

## 正確性メモ
- 生成AIが常に正しい、見逃しがゼロになる、無条件に修正するとは描かない。
- ロボットの身体はAIエージェントの視覚的な比喩。
- 既存日本語ラベルと3条件を欠落させない。

## 共通スタイル契約
- style-profile: mikuku-graphic-recording-v1
- 横長3:2、明るい不透明アイボリー、濃い文字、暖色手描き技術グラレコ。
- 主図最大、みくく1人15〜25%、短い吹き出し、物を持たない。

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
sections/002/graphic-recording.png
```
