# Section Graphic Recording Image Prompt

## Source

- section: 002
- title: GitHub で数えると、28件でした
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

# GitHub で数えると、28件でした

## 主題

- GitHub公開リポジトリの既定 branch `devel` にある `SKILL.md` を基準に数えた
- 内訳は中央リポジトリ1つの14件と、専用リポジトリ14個の14件
- 2026年7月24日時点の公開状態を写した snapshot である

## 図解キーワード

- GitHub
- `devel`
- `SKILL.md`
- 15リポジトリ
- 28件
- fixture
- fork
- 2026年7月24日時点

## 関係・流れ・対比

```text
GitHub公開リポジトリ
  ↓ 既定 branch `devel`
`SKILL.md` を確認
  ↓ fixture / fork / SKILL.md不在を除外
15リポジトリ / 28件
```

| 区分 | リポジトリ数 | Agent Skill数 |
| --- | ---: | ---: |
| 中央リポジトリ | 1 | 14 |
| 専用リポジトリ | 14 | 14 |
| 合計 | 15 | 28 |

## 図解構造

- layout-family: comparison
- primary-relation: GitHub公開状態を `SKILL.md` で絞り込み、中央1/14件と専用14/14件から合計15リポジトリ/28件へ至る対比

## グラレコ構図案

- 左: `GitHub` → `devel` → `SKILL.md` の縦の絞り込みフロー。下に `fixture / fork / SKILL.md不在は除外` を注意ボックスで置く
- 中央: 最大の比較図。上段 `中央リポジトリ 1 → 14件`、下段 `専用リポジトリ 14 → 14件` を同じ大きさで並べ、右端で `15リポジトリ / 28件` に合流させる
- 右: `2026年7月24日時点` の snapshot カードと「完成したカタログではなく、今の作業机」の短い印象メモ。みくくを右下に置く
- みくくの表情・視線: 右側で真剣に確認しつつ安心した表情。中央の2行比較と snapshot カードを見る。手は空にする
- 吹き出し: 「数え方の基準をそろえます…」

## 正確性メモ

- 数値は `1`、`14`、`14`、`15`、`28` の記事本文記載値だけを使う
- 時点は `2026年7月24日時点`。現在の件数とは表現しない
- fixture、fork、Agent Skills形式の `SKILL.md` を確認できないものを除外する

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、中央の比較図を最大化
- 背景は全面不透明の明るい白〜ごく薄いアイボリー、文字は濃色で高コントラスト
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

Additional accuracy constraint for this section: do not invent repository names, paths, URLs, or browser labels. If a repository name is shown, it must be exactly `igapyon-agent-skills`; otherwise use a generic repository icon with no name. Keep the only factual repository labels as `中央リポジトリ`, `専用リポジトリ`, `GitHub`, `devel`, and `SKILL.md`.

## Output Target

Save the generated image as:

```text
sections/002/graphic-recording.png
```
