# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: 人間の美意識と、その根底にあるユーモア
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
- Mikuku's hands and fingers are outside the scope of illustration by default. Keep Mikuku's hands and fingers outside the frame. Prefer a head-and-shoulders view and do not add hand gestures.
- include one short speech bubble based on the section summary or its `グラレコ構図案`
- do not add scenic background decoration that is not grounded in the section

## Section Summary

# 人間の美意識と、その根底にあるユーモア

## 主題

- 同じ要件でも複数の作り方があり、その選択に美意識が表れる。
- 少し引いて眺め、笑って見直すユーモアが、美意識を支えるという筆者の見方。

## 図解キーワード

- 同じ要件
- 分け方・統一・複雑さ
- ユーモア
- 美意識
- 言葉にする
- 修正の方向
- 余白

## 関係・流れ・対比

```text
同じ要件 → 分け方・統一・複雑さを選ぶ
ユーモア → 美意識 → 言葉にする → 修正の方向
小さな仕事に大がかりな仕組み？ → 少し笑って見直す
```

## 図解構造

- layout-family: flow
- primary-relation: ユーモアを土台に、美意識を言葉にし、作り方を選ぶ流れ

## グラレコ構図案

- 画像内題名: 美意識と、その根底にあるユーモア
- 左: 同じ要件を表す1つの箱から、3つの小さな構造スケッチへ枝分かれ。「分け方」「統一」「複雑さ」のラベル。下に「大がかりすぎる？」と小さく添える。
- 中央: 主図はユーモア→美意識→言葉にする→修正の方向のつながった流れ。ユーモアのそばに「少し引いて眺める」「笑って見直す」、美意識のそばに「しっくりくる」「余白」を短く添える。
- 右: 説明役のみくく1人の大きな肩から上の肖像。画面の約20%を占め、クリーム色の襟付きブラウス、手指は完全に画面外。主図や文字を髪で隠さない。
- みくくの表情・視線: 少し照れたやさしい困り顔。右側から左上の主図を見つめる。顔と胸元を自然に描き、手のジェスチャーや持ち物は加えない。
- 吹き出し: 少し笑って見直す余裕も、持ちたいですね。

## 正確性メモ

- 美意識とユーモアの関係はこの記事の見方として描く。科学的法則のように断言しない。別節の道具や役職は追加しない。
- セクション本文だけを使い、モデル名、数値、日付、価格、評価を新しく補わない。制作上の見出しやファイル名は画像内に描かない。
- 画像内題名と図解ラベルだけを描く。日本語は明瞭な濃色で、Agent Skills・MCP・GitHub と日本語の間には空白を入れる。

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長3:2、左・中央・右の3領域。主図を最大化し、適度な情報量を保つ。
- 均一に明るい白〜ごく薄いアイボリー。全面不透明、濃い茶や黒の読みやすい文字、やわらかな手描き線。淡い桃色と青緑の囲み。暗い周辺減光や汚れなし。
- みくくは説明役として読める大きさで1人、短い吹き出し1つ。手指は原則描写対象外として画面外に置き、不要な物を持たない。
- キャラクターの顔、目、茶色の長いツインテール、黒と深紅のリボンを保つ。

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
- みくくは画面の15〜25%を占める説明役として描き、短い吹き出しを含める。固定条件を変更する場合は下の deviation に理由を書く
- 日本語ラベルは短く、少数に絞る
- 長文を画像内に入れすぎない
- 明るく清潔で、Note.com や技術記事に合うビジュアル
- 写実寄り、暗い色味、無機質な企業プレゼン風は避ける
- みくくには不要な物を持たせない
- 手指は原則描写対象外として画面外に置き、説明に不要な手のジェスチャーを加えない

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
