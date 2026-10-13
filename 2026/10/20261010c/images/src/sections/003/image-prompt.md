# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: 今日やることと、この先の予定を見渡せる
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

# 今日やることと、この先の予定を見渡せる

## 主題

- day-planは、記録をまとめて今日と近い予定を確認するための一覧。
- 生成にはdaybook側のスクリプト、Node.js、依存パッケージの準備が必要。
- 利用者が「今日のday-planを作って」と依頼して生成する。

## 図解キーワード

- 今日のday-plan
- 今日取り組む作業
- 近々始まる作業
- 終了予定日が近いタスク
- 対象日を含む1週間の予定
- 予定期間を過ぎた未完了タスク
- 日程の確認が必要
- 記録をまとめる
- スクリプト / Node.js / 依存パッケージ

## 関係・流れ・対比

```text
Markdownの予定・タスク
  ↓ 「今日のday-planを作って」
daybookの生成スクリプト
  ↓
今日の作業 + 近く始まる作業 + 1週間の予定
  + 予定期間超過の未完了タスク + 日程確認が必要なタスク
```

## 役割分担・判断軸

- 事前準備: daybookに生成スクリプト、Node.js、依存パッケージを用意
- AIエージェント: 利用者の依頼でday-planを生成
- day-plan: その時点の記録をまとめる
- 利用者: 一覧から今日の一歩と先の予定を確認

## 図解構造

- layout-family: flow
- primary-relation: daybookの記録をday-planにまとめ、今日の作業と対象日を含む1週間の予定、確認が必要なタスクを見渡す

## グラレコ構図案

- 左: スクリプト・Node.js・依存パッケージの準備と「今日のday-planを作って」の依頼。
- 中央: Markdownの予定・タスクからday-planへ集約する大きな矢印。
- 右: 「今日の作業」「近々始まる作業」「終了予定日が近いタスク」「対象日を含む1週間の予定」「期間超過の未完了」「日程確認」の一覧。
- 最も大きく見せる主図: 記録からday-planへ集約され、今日と先の予定が並ぶ流れ。
- みくくの表情・視線: day-planの一覧を読者と一緒に見る落ち着いた表情。
- 吹き出し: 「今日の一歩と、先の予定を見渡せます…！」

## 正確性メモ

- 「近々の予定」は対象日を含む1週間分。
- 予定期間を過ぎた項目は未完了タスク。日程確認が必要なタスクも表示する。
- 生成スクリプト等の準備が必要。準備なしで自動生成されるように描かない。
- 実行時刻や締切をこの節から追加しない。

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

Save the generated image as:

```text
sections/003/graphic-recording.png
```
