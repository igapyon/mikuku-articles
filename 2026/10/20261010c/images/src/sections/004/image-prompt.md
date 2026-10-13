# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: 作業する日と、締切を分けて考えられる
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

# 作業する日と、締切を分けて考えられる

## 主題

- 作業予定期間と外部から決められた締切は別の情報。
- day-planは作業予定期間を基準にするため、タスク本文に書いた締切だけでは表示されない。
- 活動記録と、タスク全体の完了も別。

## 図解キーワード

- 作業予定期間
- 開始日 / 終了日
- 外部締切
- 10月12日
- 10月16日
- day-plan
- 仮の日程
- 確認が必要
- 活動記録
- タスク完了
- 交通費精算

## 関係・流れ・対比

| 分けるもの | 例・扱い |
| --- | --- |
| 作業予定日 | 交通費精算に手をつける10月12日 |
| 外部締切 | 提出の締切10月16日。タスク本文に意味を残す |
| 活動記録 | 明細をまとめた、という進捗 |
| タスク完了 | 提出など残りの作業も終わった状態 |

day-planは作業予定期間で一覧化。締切が本文にあるだけでは自動抽出しない。

## 役割分担・判断軸

- 作業をするつもりの日を開始日・終了日として記録
- 1日だけの予定では開始日と終了日を同じ日にする
- 仮置きの日程は仮と記録し、確認対象にする
- 外部締切は日付の意味がわかるようタスク本文へ書く
- 進捗の活動記録があっても、提出などが残ればタスクは未完了

## 図解構造

- layout-family: comparison
- primary-relation: 作業予定期間と外部締切、活動記録とタスク完了を別々の情報として扱う

## グラレコ構図案

- 左: 交通費精算のタイムライン。10月12日の「作業予定」と10月16日の「提出締切」を別カードにする。
- 中央: day-planへの矢印は作業予定期間から引く。タスク本文の締切から自動抽出されるような矢印は描かず、短い注意書きを付ける。
- 右: 「明細をまとめた」活動記録と「提出まで完了」のタスク状態を比較。残作業があれば未完了と示す。
- 最も大きく見せる主図: 日付のタイムラインと2つの明確な対比。
- みくくの表情・視線: 注意点をやさしく説明する表情で、二つの対比を示す。
- 吹き出し: 「作業する日と締切は、別に残します…！」

## 正確性メモ

- 交通費精算の作業予定日10月12日、提出締切10月16日。
- day-planは作業予定期間を基準にし、本文中の締切を自動では拾わない。
- 仮の日程は仮と記録して確認が必要なものとして扱う。
- 活動記録が残っても、提出などの作業が終わらなければタスク完了ではない。

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

- In the transport-expense example, October 12 is only the planned work date and October 16 is the submission deadline.
- The activity example must read `今日、交通費の明細をまとめた` and must have no date attached. Do not label this activity October 12 or imply that it happened on the planned work date.
- Keep work plan, deadline, and activity as distinct facts in separate visual elements.

Save the generated image as:

```text
sections/004/graphic-recording.png
```
