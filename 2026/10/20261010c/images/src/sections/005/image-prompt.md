# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: 会話を閉じても、記録を読み返せる
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

# 会話を閉じても、記録を読み返せる

## 主題

- daybookの記録は会話の外にあるMarkdownファイルとして残り、人が読み返して編集できる。
- 別の会話でAIエージェントが続きを手伝うときも、その記録を参照できる。
- day-planは記録から作る一覧。同じ対象日で再生成するとファイルを上書きする。

## 図解キーワード

- 会話
- Markdownファイル
- 手元に残る記録
- 人が読み返す・直す
- 別の会話
- day-plan
- 再生成
- 同じ対象日のファイルを上書き
- 残したいメモは元のタスクや予定へ

## 関係・流れ・対比

| 情報 | 役割 |
| --- | --- |
| Markdownの元記録 | 会話の外に残り、人が読み返して編集できる |
| 別の会話 | 必要に応じて元記録を参照し、作業を続けられる |
| day-plan | その時点の記録から作る一覧。同じ対象日で再生成すると上書きされる |

## 役割分担・判断軸

- 残しておきたいメモは元のタスクや予定に書く。
- day-planは記録から作る一覧として読み、長期保存したい原本とは分けて考える。
- 会話をまたいで必要な情報は、Markdownの記録から確認する。

## 図解構造

- layout-family: flow
- primary-relation: 会話から独立したMarkdownの元記録を、人・別の会話・day-planがそれぞれ使う

## グラレコ構図案

- 左: AIエージェントとの会話から、予定・タスクのMarkdown記録へ情報が残る。
- 中央: 人がMarkdownを読み返して編集し、別の会話でも記録を参照して続けられる。
- 右: 元記録からday-planを生成する流れと、同じ対象日の再生成では一覧が上書きされる注意を示す。残したいメモは元のタスク・予定に書く。
- 最も大きく見せる主図: 会話の外に残る元記録を中心にした流れ。
- みくくの表情・視線: 記録を見返す安心感を伝える。
- 吹き出し: 「残したいことは、元の記録へ書きます…」

## 正確性メモ

- 記録の形式はMarkdownファイル。
- day-planはその時点の記録から作る一覧で、再生成すると同じ対象日のファイルを上書きする。
- 会話を閉じても記録を人が読み返し、必要なら編集できる。
- 紙のノートや自動バックアップなど、記事にない保存方法を描かない。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右の3領域、主図を最大化
- 背景は均一に明るい白〜ごく薄いアイボリー、濃色の読みやすい文字、淡い手描き線
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

## Critical Example Accuracy

- Do not invent dates, filenames, or example conversation text. Show generic Markdown records labeled only with `予定`, `タスク`, and `活動記録`.
- Do not add a sample year or calendar date to the Markdown file or day-plan.
- Keep the distinction clear: the original Markdown record remains available to read and edit; regenerating day-plan overwrites the file for that same target date; notes to preserve belong in the original task or schedule.
- Show exactly one Mikuku figure in the whole poster. Use document icons or simple person symbols for the other steps; do not add miniature or duplicate Mikuku figures.

Save the generated image as:

```text
sections/005/graphic-recording.png
```
