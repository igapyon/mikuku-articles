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

# はじめに

## 主題

- 日々の予定・作業・活動の記録を、AIエージェントに手伝ってもらうための `igapyon-miku-daybook` Skill。
- 忙しいと、記録場所や項目を探して書き、あとで見返す負担が大きい。
- いつもの言葉で依頼し、今日やることと先の予定をつかみやすくする。
- daybookは個人用のMarkdown記録帳。SkillはAIエージェントが記録帳を扱うルール。

## 図解キーワード

- 日々の予定
- 取り組む作業
- やったこと
- 記録の手間
- いつもの言葉
- AIエージェント
- igapyon-miku-daybook
- Markdownの記録帳
- 今日やること
- この先の予定

## 関係・流れ・対比

```text
記録の手間・あとで書こう
  ↓ いつもの言葉で依頼
AIエージェントがSkillのルールを参照
  ↓
予定 / タスク / 活動記録をMarkdownへ
  ↓
今日とこの先をつかみやすく
```

## 役割分担・判断軸

- daybook: 個人用の予定・タスク・活動記録
- Agent Skill: AIエージェントがdaybookの記録を参照・編集するためのルール
- 利用者: いつもの言葉で依頼し、できた記録を確認
- Skillを読み、daybookの記録を参照・編集できるAIエージェントで使う

## 図解構造

- layout-family: flow
- primary-relation: 記録の手間を、いつもの言葉による依頼とAIエージェントの支援で軽くし、今日と先の予定をつかみやすくする

## グラレコ構図案

- 左: 忙しいと「あとで書こう」になりやすい記録の負担を小さく示す。
- 中央: 利用者の言葉 → `igapyon-miku-daybook` Skillを使うAIエージェント → Markdownの記録帳、の流れを最大の主図にする。
- 右: 予定・作業・やったことが残り、今日とこの先の予定をつかみやすくなる様子。
- 最も大きく見せる主図: いつもの言葉で依頼して、記録がMarkdownに残るまでの流れ。
- みくくの表情・視線: 右側で安心した優しい表情。中央の流れを見る。
- 吹き出し: 「記録を言葉でお願いできるのですね…！」

## 正確性メモ

- daybookは個人用の記録帳、SkillはAIエージェント向けのルールであり、同じものとして描かない。
- 予定・作業・活動記録を扱う。記事にない自動記録や同期機能は加えない。

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

## Critical Character Constraint

- Show exactly one Mikuku figure in the whole poster, placed as the explainer in the right region.
- In the left and center regions use icons, arrows, and record cards only. Do not draw Mikuku again as the busy user, requester, or another small character.

Save the generated image as:

```text
sections/001/graphic-recording.png
```
