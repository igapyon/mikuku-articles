# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: 「使っていない」は、失敗ではありません
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

# 「使っていない」は、失敗ではありません

## 主題

- ほとんど使っていない Skill や、まだ活用できていない Skill があっても、それだけで失敗ではない
- Agent Skill は毎日呼び出す command の一覧ではなく、特定の作業で迷わないための入口にもなる
- 価値は呼び出し回数だけでなく、必要なときに迷わず使えるか、次に育てる場所が見えるかにもある

## 図解キーワード

- 使っていない
- 失敗ではありません
- 毎日呼び出す command
- 実験的
- `igapyon-skill-compactor`
- 迷わず使える
- 次に育てる場所

## 関係・流れ・対比

```text
呼び出し回数だけで見る
  → 「使っていない」
  → 失敗と決めてしまう

必要なときの迷いにくさ・次の育成先も見る
  → 置いておく意味が見える
```

- `igapyon-skill-compactor` は、使いながら育てる実験的な例
- Skill には、今すぐ使うものだけでなく、将来の用途へ向けた seed もある

## 図解構造

- layout-family: decision
- primary-relation: 呼び出し回数だけで価値を決める見方から、迷わず使えるか・次に育てる場所が見えるかを含む見方へ切り替える判断

## グラレコ構図案

- 左: `呼び出し回数だけ` の細いものさしと、そこから出る「使っていない」のラベル。すぐに失敗と決めない注意印を置く
- 中央: 最大の分岐図。「回数だけで判断」から `迷わず使える` / `次に育てる場所が見える` へ分かれる二つの見方を描く
- 右: `igapyon-skill-compactor` を `実験的` な種のようなカードとして示す。みくくは右下で中央の分岐を見る
- みくくの表情・視線: 少し心配そうだが、安心へ向かう表情。中央の分岐と実験的カードを見る。手は空にする
- 吹き出し: 「使っていない＝失敗、ではないのです…」

## 正確性メモ

- `igapyon-skill-compactor` は実験的で、まだ十分に活用できていない例
- 呼び出し回数だけで価値を決めない、という記事の主張を描く
- 「使っていない Skill は必ず価値がある」など、記事にない断定は足さない

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、中央の判断分岐を最大化
- 明るい全面不透明の白〜薄いアイボリー、濃色ラベル、パステルの注意カード
- みくくは1人、物を持たず、短い吹き出しを1つ

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

Additional accuracy constraint for this section: do not draw any invented numeric examples, percentages, rankings, or a fictional table such as `skill-a`, `skill-b`, `skill-c`, or `skill-d`. The only number permitted in the image is a number already present in the section source; preferably use no number at all. Explain the contrast with words, arrows, icons, and the exact phrase `使っていない＝失敗ではない` instead.

## Output Target

Save the generated image as:

```text
sections/005/graphic-recording.png
```
