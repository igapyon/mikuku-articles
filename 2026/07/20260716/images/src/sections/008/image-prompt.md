# Section Graphic Recording Image Prompt

## Source

- section: 008
- title: miku-prompt-lintでできること
- section-text: sections/008/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# miku-prompt-lintでできること

## 主題
- 名前と対象を指定すると、PromptからRepository/Harnessまでをレビューできる。
- 合否や作者判定ではなく、リスクと次に確かめる点を根拠つきで整理する。

## 図解キーワード
- 呼び出し
- Prompt
- Context
- Agent Skill
- Repository/Harness
- 品質リスク
- 不足する契約
- 改善点

## 関係・流れ・対比
Skill名＋対象 → 成果物を読む → リスク・不足・改善点＋根拠
対象外: 作者判定 / 万能保証 / 単純な合格・不合格

## グラレコ構図案
- 左: 短い呼び出し例を示す入力カード。
- 中央: 4 Review Levelを通るレビュー工程。
- 右: 根拠つき所見と「次に確かめること」、下に対象外ボックス。
- みくくの表情・視線: 対象外ボックスも忘れず示す穏やかな表情。
- 吹き出し: 「不安の中身を確認しやすく」

## 正確性メモ
- 作者や生成元を判定しない。
- 静的レビューと実際のモデル実行を同一視しない。

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
- 日本語ラベルは短く、少数に絞る
- 長文を画像内に入れすぎない
- 明るく清潔で、Note.com や技術記事に合うビジュアル
- 写実寄り、暗い色味、無機質な企業プレゼン風は避ける
- みくくに物を持たせない

## Image Text Policy

- 画像内テキストは section summary の語句を短く整理して使う
- 本文の長い文をそのまま入れない
- 文字が崩れても、元記事や section-text.md は変更しない

## Output Target

Save the generated image as:

```text
sections/008/graphic-recording.png
```
