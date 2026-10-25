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

# PHP2Shellを、仕組みから

## 主題

- PHP2Shellと呼ばれる2件の脆弱性を、処理を途中でやめたあとの後片づけから読み解く。
- 条件がそろうとリモートコード実行につながることがある。

## 図解キーワード

- PHP2Shell
- 2件の脆弱性
- 処理を途中でやめる
- 後片づけ
- 何が残る？
- リモートコード実行

## 関係・流れ・対比

```text
処理を途中でやめる → 後片づけ → 何が残る？
注意: 条件がそろうとリモートコード実行
```

## 図解構造

- layout-family: flow
- primary-relation: 処理を途中でやめたあと、後片づけで何が残るかをたどる

## 役割分担・判断軸

- この章は記事の入口。後の章にあるCVE番号、具体的なメモリ機構、修正方法を混ぜない。
- 後片づけを行うたびに必ずコード実行へ至る、という関係線にはしない。

## グラレコ構図案

- 左: 大きな「処理を途中でやめる」のボックス。途中で止まった処理の短い矢印と停止記号。
- 中央: 最も大きい主図は3段階の横フロー。「処理を途中でやめる」→「後片づけ」→「何が残る？」。最後は状態の異なる抽象的なデータブロックに小さな疑問符。掃除道具や部屋ではなく、処理とデータの図として描く。
- 右: 下部にみくく。上部に「2件の脆弱性」と小さな注意欄「条件がそろうとリモートコード実行」。注意欄はフローの必然的な結末としてつながない。
- 最も大きく見せる主図: 「中断したあと」をたどる3段階フロー。題名は「PHP2Shellを、仕組みから」。
- みくくの表情・視線: 右下に約20%の大きさで1人。少し緊張しつつやさしく、中央のフローを見る。茶色の長いツインテール、黒と深紅のリボン、茶色の瞳、白い襟付きブラウス。手は自然に下へ、物を持たない。
- 吹き出し: あの…後片づけを、ひとつずつ見てみましょう。

## 正確性メモ

- section-source.mdの「はじめに」だけを根拠にする。日付、CVE番号、修正バージョン、影響規模などを追加しない。
- 「条件がそろうと」を省かない。手順やコード例は作らない。
- この設計文はそのまま印刷せず、題名・短いラベル・吹き出しだけを描く。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右の3領域、主図を最大化。明るい白〜薄いアイボリーで全面不透明。
- fully opaque background; no transparent or semi-transparent pixels
- 濃色で読める日本語。やわらかい手描き線と淡いオレンジ・ティールの囲み。暗い陰影やビネットなし。
- 同じみくくを1人、短い吹き出し1つ、物を持たない。背景の風景を加えない。

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
sections/001/graphic-recording.png
```
