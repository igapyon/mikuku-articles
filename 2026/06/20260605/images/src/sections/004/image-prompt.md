# Section Graphic Recording Image Prompt

## Source

- section: 004
- title: 魔法陣の先には、妖精さんがいる
- section-text: sections/004/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 魔法陣の先には、妖精さんがいる

## 主題

MCP の先で働く外部の道具や処理を、小さなうさぎ型の妖精さんとして見る。

## 重要マッピング

| 妖精さん | うさぎの姿 | 働き |
| --- | --- | --- |
| CLI | 明るい茶色のネザーランドドワーフ | 手元でぱたぱた動く |
| API | 白と淡いグレーのホーランドロップ | 遠くの入口で受け取る |
| database | 黒に近いチョコレート色のミニレッキス | 静かに記録を探す |
| MCP server 内の小処理 | クリーム色のジャージーウーリー | ふわっと内側で働く |

## 図解

```text
MCP = 魔法陣
  ↓
CLI / API / database / internal function
  ↓
それぞれ違う妖精さん
```

## 注意

うさぎ型の姿は比喩。本当に羽が生えている話ではない。

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

## Rabbit Fairy Continuity Rules

If this section image includes rabbit-like fairies or fairy mascots, preserve the article mapping exactly. Do not invent unrelated generic white rabbits. Do not swap roles, colors, or breeds. Do not draw humanoid fairies, Tinkerbell-like fairies, winged girls, pixies, elves, or human-shaped mascot fairies. In this article, fairy means rabbit-like fairy mascot.

- CLI: 明るい茶色のネザーランドドワーフ風。small bright light-brown Netherland Dwarf rabbit fairy, compact upright ears, local and energetic, near terminal or local tool icon.
- API: 白と淡いグレーのホーランドロップ風。white and pale-gray Holland Lop rabbit fairy, soft drooping lop ears, calm remote entrance or cloud doorway feeling.
- database: 黒に近いチョコレート色のミニレッキス風。near-black chocolate Mini Rex rabbit fairy, sleek quiet guide, near records or stacked disks.
- MCP server internal function: クリーム色のジャージーウーリー風。cream Jersey Wooly rabbit fairy, fluffy woolly appearance, small internal worker inside MCP server area.

Technical concept boxes such as tool, resource, tool schema, client, or agent may use icons, scrolls, books, terminals, servers, or robots. They must not introduce extra rabbit fairies unless those rabbits are one of the four mappings above and labeled accordingly.

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
sections/004/graphic-recording.png
```
