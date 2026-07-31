# Section Graphic Recording Image Prompt

## Source

- section: 008
- title: まだベータ版
- section-text: sections/008/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# まだベータ版

## 主題

- 記事作成時点の v0.5.0 では test 33件、成功32件、環境依存 skip 1件
- Windows-31J を維持した更新経路も test に含まれる
- 完成済みではなく、壊しやすい境界を確かめながら使う段階

## 図解キーワード

- v0.5.0
- ベータ版
- 33 tests
- 32 pass
- 1 skip
- Windows-31J 維持
- 観測を続ける

## 関係・流れ・対比

```text
33 tests = 32 pass + 1 environment-dependent skip
ベータ版 → testで境界を確認 → 観測を続ける
```

## グラレコ構図案

- 左: v0.5.0 ベータの札
- 中央: 33 / 32 / 1 のテスト結果
- 右: Windows-31J 更新経路のチェック
- みくくの表情・視線: 数字を慎重に確認する
- 吹き出し: 「まだ、確かめながら使う段階です…」

## 正確性メモ

- skip は Windows `cmd.exe` transport の1件で実行環境による

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
