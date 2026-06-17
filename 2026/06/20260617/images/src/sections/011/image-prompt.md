# Section Graphic Recording Image Prompt

## Source

- section: 011
- title: 索引ありなしで比べる
- section-text: sections/011/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 011 索引ありなしで比べる

## 主題

- index なし / ありで、画面表示上のトークン消費を比較する
- 平均では index ありのほうが低め
- ただし揺れは大きく、厳密なベンチマークではない

## 測定結果

| 条件 | 単純平均 |
| --- | ---: |
| index.json なし | 約 110.6K used |
| index.json あり | 約 82.4K used |

## 解釈

- 差分は約 28.2K used
- だいたい 25% 低め
- 毎回きれいに下がるわけではない
- 本文 Markdown を読む必要があるため、重さは残る
- 効いているのは主に探索の入口

## 図解ポイント

```text
index なし: 直接探索 → 揺れやすい
index あり: 地図 → 候補 → 本文
```

## キーワード

- 約 110.6K
- 約 82.4K
- 約 25% 低め
- 揺れあり
- 観察結果

## 吹き出し候補

「数字は揺れます。でも入口の迷い方は変わって見えます…」

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
sections/011/graphic-recording.png
```
