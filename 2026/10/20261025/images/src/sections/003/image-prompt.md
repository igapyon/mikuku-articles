# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: せっかくSkillにするなら、ほかの形式も
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

# せっかくSkillにするなら、ほかの形式も

## 主題

- 図内題名: 変換の仕事を、ひとつのSkillへ
- HTML専用の単発Skillを作る代わりに、Markdownからほかの形式へ変換する仕事をまとめる。miku-ms-office-skillsの枠組みと同梱ツールを活用する判断。

## 図解キーワード

- Markdown
- HTML変換
- Agent Skill
- miku-ms-office-skills
- 枠組み
- 同梱ツール

## 関係・流れ・対比

- 出力先ごとに増えるSkill → Markdownの変換をひとつのSkillへまとめる

## 図解構造

- layout-family: comparison
- primary-relation: 出力先ごとに増えるSkill → Markdownの変換をひとつのSkillへまとめる

## グラレコ構図案

- 左: 小さい複数カード「HTML用Skill」「ほかの形式のSkill」で、出力先ごとに増える可能性を表す。
- 中央: 最も大きい囲み「Markdownの変換をひとつに」。左からまとめる矢印。
- 右: 「miku-ms-office-skills」の箱から「枠組み」「同梱ツール」を中央のSkillへ提供する線。
- 最も大きく見せる主図: 上記のprimary-relation。左右と中央の関係を明確にする。
- みくくの表情・視線: 画面の右下、または指定がある場合は中央下。画面の20%程度の大きさで1人。やわらかな少し照れた説明表情で主図を見る。キャラの外観は正本を維持。何も持たない。自然な空の手。
- 吹き出し: ひとつにまとめられたら、よさそうです。

## 正確性メモ

- 対象セクションの本文だけに基づく。この節には四形式の列挙がない。DOCX/XLSX/PPTXやNode.js/Javaの詳細を足さず、まとめ方の判断を描く。
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
sections/003/graphic-recording.png
```
