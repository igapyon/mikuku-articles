# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: 何が起きたのか
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

# 中断のあとに残ったもの

## 主題

- 1件目は初期化が途中で止まり、未完成のデータを終了処理が使う問題。
- 2件目はデータ本体だけが解放され、残った古い参照を次のリクエストが使う問題。

## 図解キーワード

- CVE-2026-109618
- CVE-2026-109619
- 初期化
- メモリ不足
- 未完成のデータ
- 終了処理
- 古い参照
- 次のリクエスト

## 関係・流れ・対比

```text
① 初期化 → メモリ不足で中断 → 未完成のデータ → 終了処理が使用
② エラーなどで中断 → データ本体を解放・参照は残る → 次のリクエストが古い参照を使用
```

## 図解構造

- layout-family: comparison
- primary-relation: 未完成のデータを使う経路と、解放後に残った古い参照を使う経路を2段で比較する

## 役割分担・判断軸

- ① CVE-2026-109618は、同じリクエストの終了処理に残った未完成データを使う。
- ② CVE-2026-109619は、同じワーカーの次のリクエストが通常の初期化より前に古い参照を使う。
- 2つの残留物と、使用するタイミングを分ける。

## グラレコ構図案

- 左: 上段に「① CVE-2026-109618」と「初期化」。下段に「② CVE-2026-109619」と「データ本体を解放」。
- 中央: 上段はオレンジの「メモリ不足で中断」→半分だけ埋まった「未完成のデータ」→「終了処理が使用」。下段はティールの空のメモリ領域へ「古い参照」の矢印が残り、点線のリクエスト境界を越えて「次のリクエストが使用」へ。下段だけに注記「通常の初期化より前」。
- 右: 上段の結末を「未完成のまま使用」、下段の結末を「解放済みメモリへアクセス」と短く示す。右下にみくく。
- 最も大きく見せる主図: 2段のフローと、未完成のデータ／古い参照の対比。どちらも単なる同一の空箱にしない。
- みくくの表情・視線: 右下に約20%の大きさ。少し心配しつつ2つの流れを見比べる。同じ茶色のツインテール、黒と深紅のリボン、茶色の瞳、白い襟付きブラウス。物を持たない。
- 吹き出し: うぅ…止まったあとにも、残るものがあったのですね。

## 正確性メモ

- この章にないコード実行の一般機構、修正方法、攻撃条件やバージョンを追加しない。
- 1件目の発生を次のリクエストへ移さない。2件目のデータ本体は解放済みであり、残るのは参照。
- CVE識別子の数字を正確に描く。1件目109618、2件目109619。
- 図のラベルと吹き出しだけを使い、設計文全体を小さな注記として印刷しない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右、主図を最大化。明るい白〜薄いアイボリー。
- fully opaque background; no transparent or semi-transparent pixels
- 濃色の短い文字、やわらかい手描き線、オレンジとティールの淡い囲み。暗い陰影なし。
- みくくは同じ1人、短い吹き出し1つ、物を持たない。

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
sections/003/graphic-recording.png
```
