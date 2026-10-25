# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: なぜコード実行につながるのか
- section-text: sections/004/section-text.md
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

# なぜコード実行につながるのか

## 主題

- 解放したメモリ領域が別のデータに再利用されると、古い参照を使う処理は以前の構造として扱ってしまう。
- 食い違いを利用できる条件がそろうと、メモリの読み書きや実行の流れが壊れ、コード実行につながる場合がある。
- 成立条件はPHPの動かし方やアプリケーションにより異なり、実行権限はWebワーカーの権限。

## 図解キーワード

- 解放後使用
- 古い参照
- 別のデータ
- 以前の構造
- コード実行
- 成立条件
- Webワーカーの権限
- mod_php
- PHP-FPM

## 関係・流れ・対比

```text
データを解放 → 同じ領域に別のデータ → 古い参照は以前の構造として扱う
                                       ↓ 条件がそろうと
                               メモリや実行の流れの破綻 → コード実行
```

## 図解構造

- layout-family: flow
- primary-relation: 同じメモリの場所で中身が変わっても、古い参照が以前の構造として扱う食い違いを示す

## 役割分担・判断軸

- メモリの場所は同じでも、古い参照が想定する構造と現在のデータは異なる。
- 未修正のmod_phpではメモリ不足からの経路、未修正のPHP-FPMではエラー後に残った参照を次のリクエストが使う経路がある。
- すべての解放後使用が必ずコード実行になるとは描かない。

## グラレコ構図案

- 左: 「解放後使用」を主題に、薄いオレンジのデータAが置かれたメモリ箱と「古い参照」の矢印。データAを解放した状態を短く示す。
- 中央: 最大の主図は同じ位置のメモリ箱にティールの「別のデータ」が入った図。古い参照の先にオレンジの点線の想定枠「以前の構造」、実際のティールのデータとの差を見せる。記号だけでなく「場所は同じ、中身は違う」と短く記す。
- 右: 主図から「条件がそろうと」→「コード実行」の小さな注意ボックスへ。近くに「成立条件は環境で異なる」「実行権限はWebワーカーの権限」。右下にみくく。
- 最も大きく見せる主図: 古い参照の想定と、再利用された実際のデータの食い違い。下部に小さな補足2枠「未修正のmod_php：メモリ不足からの経路」「未修正のPHP-FPM：次のリクエストへ残る参照」。
- みくくの表情・視線: 右下に約20%の大きさで1人、少し考える表情で食い違いの図を見る。同じ茶色の長いツインテール、黒と深紅のリボン、茶色の瞳、白い襟付きブラウス。手は下端に自然に置き、物を持たない。
- 吹き出し: あの…同じ場所でも、中身はもう違うのですね。

## 正確性メモ

- この章の説明を模式図にする。実在のメモリアドレス、データ構造名、コード、コマンド、攻撃ペイロードは追加しない。
- Aは図上の識別用。具体的な実装を示す数値や構造は作らない。
- 環境差と権限の限定を残す。mod_phpとPHP-FPMを同一の成立条件にまとめない。
- WordPressでの実証や攻撃試行観測は本文にあるが、主図を明快にするため数値や報告の年表を追加しない。
- 設計メタデータは印刷しない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右、主図を最大化。均一に明るい白〜薄いアイボリー。
- fully opaque background; no transparent or semi-transparent pixels
- 濃色の日本語、やわらかい手描き線。オレンジの想定枠とティールの実データ。暗い陰影なし。
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
sections/004/graphic-recording.png
```

## Post-generation accuracy correction

Edit the provided existing Japanese infographic. Preserve its full 3:2 composition, title, process diagrams, arrows, colors, other labels, Mikuku's exact identity and pose, and the bright fully opaque white/ivory background. Do not redesign the infographic.

Make only these small corrections:

1. In the left orange panel, the lower caption currently reads 「データAを解放（メモリが空になる）」. Replace it with exactly 「データAを解放（領域を再利用できる）」. Keep the two-line caption layout and font size. Freeing memory must not imply that its bytes have been erased or zeroed.
2. In the small paragraph at the upper right, replace its first line 「解放したメモリ領域が別のデータに再利用されると」 with 「解放後使用では、解放した領域が再利用されると」. Keep the remaining explanation and the conditional code-execution wording unchanged. This adds the section's technical term without altering the relationship.
3. In the lower middle box titled 「実行権限はWebワーカーの権限」, replace only the blue-uniform human worker icon with a simple small software-process rectangle containing a gear. Keep the adjacent monitor/server icons, the Webワーカー label, the heading, and the rights explanation unchanged. Webワーカー here is a software process, not a human person.

Keep every other element and all text unchanged. Keep exactly one Mikuku character, long brown twin-tails and black/deep-red ribbons, warm brown eyes, white blouse, empty hands, and the existing speech bubble. No new characters or decorative scenery. fully opaque background; no transparent or semi-transparent pixels. Keep all Japanese text dark, crisp, and legible.
