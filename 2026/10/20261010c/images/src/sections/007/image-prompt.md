# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: 朝に予定を確認するきっかけも作れる
- section-text: sections/007/section-text.md
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

# 朝に予定を確認するきっかけも作れる

## 主題

- 任意のGitHub Actions設定で、day-planを指定したGitHub Issueへ投稿できる。
- 標準設定は日本時間の午前6時ごろが目安だが、遅延や未実行もあり得る。
- まず会話で記録を残してday-planを使い、必要なら後から通知を追加できる。

## 図解キーワード

- 任意の通知
- GitHub Actions
- day-plan
- 指定したGitHub Issue
- 日本時間 午前6時ごろ
- 遅延・未実行の可能性
- 投稿先はリポジトリに合わせて設定
- 会話で記録 → day-plan → 必要なら通知

## 関係・流れ・対比

| 項目 | 扱い |
| --- | --- |
| 投稿内容 | day-plan |
| 投稿先 | 設定したGitHub Issue |
| 実行時刻 | 標準設定は日本時間の午前6時ごろが目安。遅延や未実行もあり得る |
| 導入順 | 会話で記録しday-planを確認してから、必要に応じて通知を追加 |

## 役割分担・判断軸

- GitHub Actionsの仕組みは利用するdaybookリポジトリに設定する。
- 投稿先のIssueなどはリポジトリに合わせて設定する。
- 朝の確認に役立つと判断した場合に、通知機能を追加する。
- 標準スケジュールを毎朝必ず届く保証として扱わない。

## 図解構造

- layout-family: flow
- primary-relation: day-planを任意のGitHub Actionsから設定済みIssueへ投稿し、段階的に導入できる

## グラレコ構図案

- 左: 会話で記録を残し、day-planを作って確認する。
- 中央: 任意のGitHub Actionsがday-planを設定済みのGitHub Issueへ投稿する。
- 右: 朝にIssueを確認する様子と、「午前6時ごろが目安」「遅延・未実行もあり得る」の注記を配置する。
- 最も大きく見せる主図: day-planからGitHub Actionsを経て指定Issueへ届く矢印。通知は追加機能と示す。
- みくくの表情・視線: 設定の注意点をやさしく説明し、Issueへ視線を向ける。
- 吹き出し: 「通知は、必要になってから足せます…」

## 正確性メモ

- 投稿先は指定したGitHub Issueで、利用リポジトリに合わせて設定する。
- 標準設定の目安は日本時間午前6時ごろ。
- GitHub Actionsのスケジュール実行には遅延や未実行があり得る。
- 毎朝の定刻到着や、通知機能が必須であるかのように描かない。

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

## Critical Accuracy and Character Constraints

- Show exactly one Mikuku character in the entire image; do not repeat her in the Issue mockup or anywhere else. Use generic interface cards for the GitHub Issue.
- Preserve the distinction between the optional GitHub Actions notification and the basic conversation/day-plan workflow.
- The schedule is only `日本時間 午前6時ごろが目安`; explicitly retain that delays or missed runs can happen. Do not imply guaranteed delivery.

Save the generated image as:

```text
sections/007/graphic-recording.png
```
