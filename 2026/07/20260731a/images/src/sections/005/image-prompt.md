# Section Graphic Recording Image Prompt

## Source

- section: 005
- title: 読むときだけでなく、最後まで同じ入口を使う
- section-text: sections/005/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 読むときだけでなく、最後まで同じ入口を使う

## 主題

- 操作は search / read / create / update / delete の五つ
- 読取だけ専用 CLI にして、更新を通常の UTF-8 patch tool へ戻してはいけない
- encoding-sensitive と分かった path は検証・競合回復まで同じ CLI を使う

## 図解キーワード

- search
- read
- create
- update
- delete
- 最後まで同じ入口
- 必要な path だけ

## 関係・流れ・対比

```text
安全: search → read → update → verify（同じ CLI）
危険: read（専用 CLI）→ update（UTF-8 patch tool）
```

## グラレコ構図案

- 左: search と read
- 中央: 分岐せず続く専用 CLI の一本道
- 右: update・verify・競合回復
- みくくの表情・視線: 一本道を指ささず、視線で追う
- 吹き出し: 「途中で、いつもの道具へ戻らないでください…！」

## 正確性メモ

- 普通の UTF-8 ファイルまで専用 CLI へ寄せない

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
sections/005/graphic-recording.png
```
