# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: PHPの処理を担当するワーカー
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

# ワーカーは続く、データは入れ替わる

## 主題

- PHP-FPMはPHPを実行するプロセスを起動・管理する仕組み。
- Webサーバーからの依頼をワーカーが担当し、同じワーカーが次のリクエストも続けて処理することがある。
- ワーカーの生存期間と、リクエストごとのデータの有効期間を区別する。

## 図解キーワード

- Webサーバー
- PHP-FPM
- ワーカー
- リクエスト
- データを作る
- 使い終えたメモリを解放
- データは入れ替わる

## 関係・流れ・対比

```text
Webサーバー → PHP-FPMが管理するワーカーへ処理を依頼
同じワーカー: ━━━━━━━━━━━━━━━━━━━━━━
リクエストA: データを作る → 使う → メモリを解放
リクエストB:                          データを作る → 使う → メモリを解放
```

## 図解構造

- layout-family: flow
- primary-relation: 続いて動くワーカーの時間軸の中で、リクエストごとのデータが作られて解放される

## 役割分担・判断軸

- PHP-FPM: FastCGI Process Manager。プロセスを起動・管理する。
- ワーカー: 実行用プロセスとして処理を担当する。
- データ: リクエストごとに作られ、使い終えたメモリは解放される。
- 同じワーカーが続けて担当する「ことがある」という留保を残す。

## グラレコ構図案

- 左: 小さな「Webサーバー」から処理依頼の矢印。その先に「PHP-FPM」の管理枠。
- 中央: 最大の主図は1本の長いワーカーの枠と時間軸。枠の上に「同じワーカーが続けて担当することがある」。中には左からリクエストA、続いてリクエストB。それぞれ「データを作る」→「使う」→「メモリを解放」という別々の短いバーを置く。AとBを同時実行の上下並行処理にしない。
- 右: 右下にみくく、右上に短い要点「ワーカーは続く」「データは入れ替わる」。
- 最も大きく見せる主図: ワーカーの長い生存期間に対して、A・Bのデータの短い生存期間が順番に現れる時間軸。
- みくくの表情・視線: 右下に約20%の大きさで1人、少し考える表情で時間軸を見る。同じ茶髪の長いツインテール、黒と深紅のリボン、茶色の瞳、白い襟付きブラウス。物を持たず、手は下端に自然に置く。
- 吹き出し: えっと…ワーカーとデータでは、寿命が違うのですね。

## 正確性メモ

- この章の内容だけを描く。ここではエラー、古い参照、CVE、修正方法を説明しない。
- データが解放されることと、プロセス自体が終了することを同じ記号にしない。
- 複数ワーカーの並列度、具体的なリクエスト数、サーバー構成は追加しない。A・Bは順次処理を説明する図上の識別子。
- 設計用メタデータは印刷せず、短いラベルと吹き出しを使う。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右、主図を最大化。均一に明るい白〜薄いアイボリー。
- fully opaque background; no transparent or semi-transparent pixels
- 濃色の文字、やわらかい手描き線。AとBはオレンジ・ティールの差で見分ける。暗い周辺減光なし。
- 同じみくくを1人、吹き出し1つ、物を持たない。

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
sections/002/graphic-recording.png
```
