# Section Graphic Recording Image Prompt

## Source

- section: 008
- title: 記事執筆までが、今回の開発だった
- section-text: sections/008/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 記事執筆までが、今回の開発だった

## 主題

- 記事は開発後のおまけではなく、設計と製造を読み直す工程
- 書くことで、作業中に見えていなかった結論が言葉になる
- 言葉になった知見を Agent Skills と次の開発へ戻せる

## 図解キーワード

- 記事は振り返り工程
- 設計を読み直す
- 製造を読み直す
- 見えなかった結論
- 言葉になる
- 知見
- Agent Skills へ戻す
- 次の開発

## 関係・流れ・対比

```text
設計 → 製造 → 記事で振り返る
                 ↓
          見えなかったことが言葉になる
                 ↓
          Agent Skills へ知見を残す
                 ↓
              次の開発
```

- 一回の開発は上から下へ
- 得た知見は次の開発の上流へ

## グラレコ構図案

- 左: 設計図と製造成果物
- 中央: 記事を書くことで内容を読み直す鏡のような図
- 右: 言葉・知見が Agent Skills と次の開発へ循環、みくく
- みくくの表情・視線: 書きながら結論を見つけた穏やかな表情
- 吹き出し: 「記事を書くと、見えていなかった知見が言葉になります…」

## 正確性メモ

- 記事執筆を実装の代替として描かない
- 記事から得た知見は、必要なら Agent Skills へ戻せる
- 記事中の「何がまだベータ版か」は整理対象の例

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
