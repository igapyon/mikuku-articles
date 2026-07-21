# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: 気軽に作れるけれど、制限は強い
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 気軽に作れるけれど、制限は強い

## 主題

- Agent Builder と Gem Classic には、登録件数・サイズ・参照範囲などの制限がある。
- 「登録できた」と「必要な情報をいつでも見つけられる」は同じではない。
- 実際の上限や挙動は、利用環境とサービス画面でも確認する必要がある。

## 図解キーワード

- 登録できる
- 参照される
- 同じではない
- 件数・サイズ
- コンテキスト
- 利用環境で確認

## 関係・流れ・対比

| 登録 | 回答時の参照 |
| --- | --- |
| ファイルを置ける | 必要部分が必ず使われるとは限らない |

## グラレコ構図案

- 左: 「登録 OK」の箱に収まった資料。
- 中央: 虫眼鏡と限られたコンテキスト枠。
- 右: 「必要情報を発見？」という確認マークとテスト用の質問。
- みくくの表情・視線: 左右を見比べ、「同じではない」を慎重に指し示す。
- 吹き出し: 「登録できても、全部が毎回見えるとは限りません」

## 正確性メモ

- 数値は多く入れず、登録と参照の違いを中心にする。
- Agent Builder の観察上の感想を公式仕様として描かない。
- Gem Classic も全内容が毎回考慮されるとは限らない。

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
sections/003/graphic-recording.png
```
