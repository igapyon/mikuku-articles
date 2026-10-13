# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
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

# はじめに

## 主題

- 必要な決め事が、使う場面で届かないことがある。
- 文書をMarkdownに整え、Agent Skillsにする。
- 対応エージェントの点検・判断材料・次の作業につなぐ。

## 図解キーワード

- 規約・ルール・チェックシート
- 記憶頼み
- 読むのが後回し
- Markdown
- Agent Skills
- 文書に沿って点検
- 判断材料
- 許可された範囲で修正

## 関係・流れ・対比

```text
必要な文書（どこを見る？／記憶頼み）
  → Markdownに整える → Agent Skills
  → 対応エージェント → 点検／判断材料／次の作業
```

- 静的なドキュメント → 実務の中で働く文書。

## 図解構造

- layout-family: flow
- primary-relation: 規約・ルール・チェックシート → Markdown → Agent Skills → 対応エージェントによる点検・判断材料・次の作業

## グラレコ構図案

- 左: 規約・ルール・チェックシートの3枚の紙アイコン。「どこを見る？」「記憶頼み」「読むのが後回し」の小さな困り事の囲み。人物を追加しない。
- 中央: 最大の主図。文書からMarkdownへ、Agent Skillsへ、対応エージェントへ太い矢印でつなぐ。その下に「文書に沿って点検」「判断材料」「次の作業」の3つの出力枠。修正は小さく「許可された範囲で修正」と付記。
- 右: みくくを右下に約20%の大きさで1人。上に短い吹き出し。主図を説明するため、左側へ視線を向ける。
- みくくの表情・視線: やさしく少し困り眉、左上の流れを見る。持ち物なし、両手は画面外でもよい。
- 吹き出し: あの…文書を仕事につなげるんです。

## 正確性メモ

- この章だけの内容を使う。修正は許可された範囲。漏れゼロ・全自動などを足さない。
- 別章の更新サイクルや修正の3条件はここに足さない。
- モデル名、価格、日付、生成環境は描かない。
- 描く文字はタイトル「はじめに」と指定した短いラベル、吹き出しのみ。内部見出しやメタデータは描かない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右、主図最大。均一に明るい白〜薄いアイボリー、濃色文字、淡い暖色、やわらかい手描き線、ホワイトボード解説風。
- みくくは説明役として読める大きさで1人。黒いリボンと深赤の縁、栗色の長いツインテールを維持。短い吹き出し1つ、物を持たない。
- 背景全面不透明。周辺減光や文字の背後の陰影なし。

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
sections/001/graphic-recording.png
```
