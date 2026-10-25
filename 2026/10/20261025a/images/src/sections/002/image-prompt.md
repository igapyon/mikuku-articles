# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: Markdownを、ちょっとHTMLで確認したかった
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

# Markdownを、ちょっとHTMLで確認したかった

## 主題

- 図内題名: ちょっとHTMLで確認したい
- Markdownビューアーはいろいろある。そのうえで、MarkdownをHTMLファイルへ変換してブラウザで確認できる小さな道具が欲しかった。

## 図解キーワード

- Markdown
- miku-md2html
- HTMLファイル
- ブラウザ
- ちょっと確認

## 関係・流れ・対比

- Markdown → miku-md2html → HTMLファイル → ブラウザで確認

## 図解構造

- layout-family: flow
- primary-relation: Markdown → miku-md2html → HTMLファイル → ブラウザで確認

## グラレコ構図案

- 左: 小さな注記「ビューアーはいろいろある」とMarkdown書類。
- 中央: 最も大きい主図に「miku-md2html」の変換箱を置き、左のMarkdownから右のHTMLへ一方向に結ぶ。
- 右: HTMLファイルと、そのファイルをブラウザで開いて確認するプレビュー。架空の記事文章は描かず見出しと本文の抽象線。
- 最も大きく見せる主図: 上記のprimary-relation。左右と中央の関係を明確にする。
- みくくの表情・視線: 画面の右下、または指定がある場合は中央下。画面の20%程度の大きさで1人。やわらかな少し照れた説明表情で主図を見る。キャラの外観は正本を維持。何も持たない。自然な空の手。
- 吹き出し: ちょっと確認したいときに、ちょっと使えます。

## 正確性メモ

- 対象セクションの本文だけに基づく。Office形式やSkillの内部構成は描かない。主題はHTMLの小さな確認用途だけ。
- 設計文は印刷せず、題名・短いラベル・吹き出しだけを画像内に描く。出力形式カード同士を連続変換する矢印を描かない。足りない情報を別セクションから補わない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右の3領域、主図を最大化
- 均一に明るい白〜薄いアイボリー。濃色の読みやすい文字。淡い暖色、ティールの囲み、手描き線と矢印。暗い陰影やビネットなし。
- fully opaque background; no transparent or semi-transparent pixels
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
sections/002/graphic-recording.png
```
