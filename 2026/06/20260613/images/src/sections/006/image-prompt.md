# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: たまには入口を整え直す
- section-text: sections/006/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 006 たまには入口を整え直す

## 主題

入口は一度作れば終わりではなく、変化に合わせて整え直す必要がある。

## 入口が見えにくくなる理由

- 機能が増える
- 仕様が変わる
- 記事が増える
- README.md や TODO.md に追記が重なる
- プロンプトに注意事項が増える
- index.json やリンクが古くなる

## うまく読めないサイン

- 入口が見つからない
- 見出しが抽象的すぎる
- 検索で拾える言葉がない
- README.md とコードがずれている
- TODO.md に古い方針が残る
- 確認場所が分からない
- テスト、ビルド、再現手順への入口がない

## 整え直すもの

- 入口を足す
- 見出しを直す
- 不要な説明を削る
- 検証方法を足す
- 正とする仕様へのリンクを残す
- 古い TODO.md を畳む

## 循環

```text
読みにくい
  ↓
入口を直す
  ↓
次に見つけやすい
  ↓
作業が安定する
```

## 吹き出し案

「入口そのものも、たまに整え直す必要があるのです…」

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
sections/006/graphic-recording.png
```
