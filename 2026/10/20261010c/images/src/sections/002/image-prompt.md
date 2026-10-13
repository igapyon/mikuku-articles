# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: 思いついたとき、いつもの言葉で残せる
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

# 思いついたとき、いつもの言葉で残せる

## 主題

- 自然な言葉の依頼を、予定・タスク・活動記録の適切な記録へ振り分ける。
- 同じタスクがある場合は、既存記録を探してから扱う。
- AIエージェントが追加・更新し、利用者はできた記録を確認する。

## 図解キーワード

- いつもの言葉
- 練習会
- 交通費精算
- 活動記録
- 予定
- タスク
- Markdown
- 既存タスクを検索
- 記録を確認

## 関係・流れ・対比

| 言葉での依頼 | 記録先 |
| --- | --- |
| 10月15日19時〜21時、○○ホールで練習会 | 予定 |
| 交通費精算、作業予定10月12日、提出締切10月16日 | タスク |
| 今日、交通費の明細をまとめた | 活動記録 |

依頼 → 内容に合う記録種別 → 既存タスクを確認 → Markdownへ追加・更新 → 利用者が確認。

## 役割分担・判断軸

- 利用者: 内容を自然な言葉で伝え、できた記録を確認
- AIエージェント: 内容に合う予定・タスク・活動記録を選ぶ
- 同じタスクがあるか、追加前に既存の記録を探す
- 「作業日」と「提出締切」の意味は混ぜずに扱う

## 図解構造

- layout-family: cards
- primary-relation: 3種類の自然言語依頼を内容に合う予定・タスク・活動記録へ振り分け、Markdownに残す

## グラレコ構図案

- 左: 3つの短い依頼カード。日付・時刻・会場、作業予定日・提出締切、今日したことの例を記事どおりに記す。
- 中央: AIエージェント + `igapyon-miku-daybook` Skillを大きく置き、依頼から記録種別へ矢印で分岐。
- 右: 「予定」「タスク」「活動記録」のMarkdownカード。タスク追加前に同じ記録を探す小さな確認を示す。
- 最も大きく見せる主図: 依頼内容から3種類の記録先への対応図。
- みくくの表情・視線: 下部または右端から記録カードを説明する、穏やかな表情。
- 吹き出し: 「言葉で伝えて、できた記録を確認します…！」

## 正確性メモ

- 会場は記事のプレースホルダー「○○ホール」のまま扱う。
- 練習会は10月15日19時から21時。
- 交通費精算の作業予定は10月12日、提出締切は10月16日。
- 活動記録は「今日、交通費の明細をまとめた」。日付を勝手に補わない。
- 「出張」「領収書」など記事にない内容を加えない。

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
sections/002/graphic-recording.png
```
