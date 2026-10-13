# Section Graphic Recording Image Prompt

## Source

- section: 008
- title: おわりに
- section-text: sections/008/section-text.md
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

# おわりに

## 主題

- `igapyon-miku-daybook` は、日々の予定や作業をAIエージェントと一緒に整える小さなSkill。
- いつもの言葉で予定を残し、今日やることや先の予定を見渡し、手元に残る記録をあとから読み返せる。
- 予定を一つ記録することから始め、覚えておく負担を軽くする。

## 図解キーワード

- `igapyon-miku-daybook`
- 日々の予定・作業
- AIエージェントと一緒に整える
- いつもの言葉で記録
- 今日やること・この先の予定
- あとから読み返せる記録
- 予定を一つ残す
- 覚えておく負担を軽くする

## 関係・流れ・対比

| 使い方 | 得られること |
| --- | --- |
| 予定をいつもの言葉で残す | 今日の作業や先の予定を見渡せる |
| 記録を手元に残す | あとから読み返せる |
| 予定を一つから始める | 頭の中で覚えておく負担を軽くする助けになる |

## 役割分担・判断軸

- AIエージェントと一緒に予定や作業を整える。
- まず一つの予定をいつもの言葉で依頼してみる。
- 記録を続ける手間を減らし、今日の一歩を考えるために使う。

## 図解構造

- layout-family: summary
- primary-relation: 一つの予定を自然な言葉で記録し、見通しと記録を得て、覚えておく負担を軽くする

## グラレコ構図案

- 左: 思いついた予定を、AIエージェントにいつもの言葉で伝える。
- 中央: daybookの記録と一覧で、今日やること・この先の予定が見える。
- 右: あとから記録を読み返し、予定を頭の中だけで抱えずに今日の一歩を考える。
- 最も大きく見せる主図: 「予定を一つ記録 → 見通す → あとで読み返す」のやさしい循環。
- みくくの表情・視線: 読者に小さな一歩を勧める、控えめで親しみやすい表情。
- 吹き出し: 「まずは予定を一つ、残してみませんか…」

## 正確性メモ

- `igapyon-miku-daybook` の役割は予定や作業をAIエージェントと一緒に整えること。
- 記事で紹介した記録・見通し・読み返しの価値をまとめる。
- 時間削減量や自動実行範囲など、本文にない効果を数値や保証で追加しない。

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

- Do not invent calendar dates, task names, meeting names, or project details. Show only generic labels such as `今日やること`, `この先の予定`, and `記録`.
- Keep the summary grounded in the article: one natural-language request can start the workflow; the user can see today's work and future plans and later reread saved records.
- Do not imply a guaranteed amount of time saved or fully automatic work.
- Show exactly one Mikuku in the whole poster. Use icons and simple record cards in the other regions; do not add miniature or duplicate Mikuku figures.

Save the generated image as:

```text
sections/008/graphic-recording.png
```
