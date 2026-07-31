# Section Graphic Recording Image Prompt

## Source

- section: 007
- title: GPT-5.6 Sol Ultra を最大限使ったから、完成まで持っていけた
- section-text: sections/007/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# GPT-5.6 Sol Ultra を最大限使ったから、完成まで持っていけた

## 主題

- 難所は CLI を作ることだけでなく、AI agent に読ませ、選ばせ、最後まで使わせること
- GPT-5.6 Sol Ultra と対話し、曖昧な境界と test で固定する契約を整理した
- GPT-5.5 Medium のときには実現できなかった繊細な設計を、現実的な労力で完成へ運べた

## 図解キーワード

- AI agent に読んでもらう
- Skill 発火
- 同じ入口
- revision
- 曖昧な境界
- test で固定
- 対話して仕様を作る

## 関係・流れ・対比

```text
対話 → 曖昧さを発見 → 仕様を整理 → testで固定 → 完成
GPT-5.5 Medium の経験 → GPT-5.6 Sol Ultra で完成へ
```

## グラレコ構図案

- 左: 小さな歯車として並ぶ設計課題
- 中央: 人間と Sol Ultra の対話で仕様を組み立てる流れ
- 右: test のチェックを通り完成する橋
- みくくの表情・視線: 少し緊張しながら完成した橋を見る
- 吹き出し: 「対話しながら、繊細な仕様を形にしました…」

## 正確性メモ

- モデルへ任せれば無条件に正しいとは書かない
- 仕様・差分・test は対話のなかで確認した

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
