# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: v0.5.0としてリリースした
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# v0.5.0としてリリースした

## 主題
- 複数モデルの役割分担による更新を v0.5.0 としてリリースした。
- SkillはSKILL.mdだけでなく、参照資料・配布・別環境での発見まで確認して使い始められる。

## 図解キーワード
- v0.5.0
- SKILL.md
- 参照資料
- インストール
- 配布
- 別環境
- 動作検証継続
- 小さな区切り

## 関係・流れ・対比
SKILL.md → 参照資料 → 配布可能 → 別環境で発見可能 → v0.5.0 → 検証継続

## グラレコ構図案
- 左: Skill構成ファイルが箱へまとまる工程。
- 中央: v0.5.0 のリリース旗。
- 右: 「完成保証ではない」「検証継続」の注意ボックス。
- みくくの表情・視線: 小旗を見て控えめに喜びつつ、注意書きも示す表情。
- 吹き出し: 「小さいけれど、ちゃんと区切りです」

## 正確性メモ
- すべてのプロンプトを正しく判定できるとは表現しない。
- リリース名は miku-prompt-lint-skills v0.5.0。

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
sections/007/graphic-recording.png
```
