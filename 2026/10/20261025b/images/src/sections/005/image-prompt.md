# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: どこを直したのか
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

# 止める場所と、次へ残す状態

## 主題

- メモリ制限に達した際は、安全な地点で処理を止める。
- さらに高いメモリ上限に達した場合は、プロセスを終了する。
- 内部状態をリセットし、次のリクエストへ古い参照を持ち越さない。

## 図解キーワード

- メモリ制限
- 安全な地点
- さらに高い上限
- プロセス終了
- 内部状態のリセット
- 古い参照
- 次のリクエスト

## 関係・流れ・対比

```text
メモリ制限に達した場合      → 安全な地点で停止
さらに高い上限に達した場合 → プロセス終了
内部状態のリセット         → 古い参照を次のリクエストへ持ち越さない
```

## 図解構造

- layout-family: decision
- primary-relation: メモリ上限に応じた停止方法と、古い参照を残さない内部状態のリセットを分けて示す

## 役割分担・判断軸

- 止める場所: 処理を安全な地点で止める。
- さらに高い上限: その場合はプロセスを終了する。
- 次へ残す状態: 古い参照を持ち越さないようリセットする。
- 2つの停止条件を、毎回必ず順番に行う作業としてつながない。

## グラレコ構図案

- 左: 「メモリ上限」の判断入口から、上と下の2条件へ分かれる。上は「メモリ制限に達した場合」、下は「さらに高い上限に達した場合」。
- 中央: 最大の主図は条件ごとの2本の矢印。上はオレンジの枠「安全な地点で停止」、下は淡い赤の枠「プロセス終了」。2枠同士を順番の矢印で結ばない。
- 右: 右下のみくくが2つの停止条件と下端のリセット欄を見る。上部に短い要点「止める場所」と「次へ残す状態」。
- 最も大きく見せる主図: 上限に応じた2つの停止条件の分岐と、下端の独立した緑の帯「内部状態のリセット」→「古い参照を持ち越さない」→「次のリクエスト」。最後の流れに古い参照が通過しないことを明確にする。
- みくくの表情・視線: 右下に約20%の大きさで1人、慎重に説明するやさしい表情。同じ長い茶色のツインテール、黒と深紅のリボン、茶色の瞳、白い襟付きブラウス。物を持たず、手は下端に自然に置く。
- 吹き出し: は、はい…止める場所と、残す状態の両方なのですね。

## 正確性メモ

- この章にある修正の考え方だけを描く。具体的な上限値、設定名、修正バージョン、更新コマンドは追加しない。
- 安全な停止をしたら必ずプロセス終了する、という一本道にしない。
- 全リクエストでプロセスが終了するように見せない。
- 修正による参照のリセットは、処理を停止する条件とは別の修正点として示す。
- 設計メタデータは印刷しない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右、主図を最大化。均一に明るい白〜薄いアイボリー。
- fully opaque background; no transparent or semi-transparent pixels
- 濃色で明瞭な文字、やわらかい手描き線、淡いオレンジ・緑・赤の枠。暗い陰影なし。
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
sections/005/graphic-recording.png
```

## Final pose correction (supersedes earlier hand-position wording)

Edit the supplied existing Japanese infographic. Preserve its full 3:2 canvas, exact title, every Japanese label and speech bubble, all process diagrams, arrows, color scheme, and the existing position and size of Mikuku at the lower right. This is a localized correction to her pose only.

Remove the clasped hands and every visible finger at the lower right. Mikuku's arms are lowered and remain entirely below the bottom edge of the poster. Continue her white blouse and brown hair naturally through the region previously occupied by the hands. Keep her face, expression, gaze, collar, hair shape, long chestnut twin-tails, black/deep-red hair ribbons, and overall identity unchanged.

Absolutely no hands, fingers, palms, wrists, or forearms may be visible anywhere in the image. Both hands and arms are outside the frame. Do not replace the clasped hands with a different hand gesture. Do not introduce an object, a covering prop, a blur, an extra box, or a cutout to hide them. Keep the poster layout and diagram area intact; do not crop the whole image or shrink Mikuku.

All Japanese text must remain verbatim and legible, especially the two memory-limit branches, the separate internal-state-reset flow, and 「は、はい…止める場所と、残す状態の両方なのですね。」. Keep exactly one Mikuku, no held objects, and the uniformly bright white/very pale ivory background. fully opaque background; no transparent or semi-transparent pixels.
