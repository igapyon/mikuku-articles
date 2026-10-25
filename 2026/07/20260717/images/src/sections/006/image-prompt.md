# Section Graphic Recording Image Prompt

## Source

- section: 006
- title: Knowledge sourceモードを追加する
- section-text: sections/006/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# Knowledge sourceモードを追加する

## 主題

会話用の指示を外し、Knowledge sourceへ登録しやすい中立的なMarkdownを生成する新しい出力モード。

## 図解キーワード

- --mode knowledge-source
- knowledge-001.md / knowledge-002.md
- knowledge-index.mdは管理用
- 会話用指示を含めない
- 行範囲・文字オフセットで追跡
- 登録や変換は呼び出し元の役割

## 関係・流れ・対比

中央の同じ入力テキストから、左のhandoff「会話の案内あり」と右のknowledge-source「資料を静かに置く」へ分岐。右側では登録候補と管理用indexを明確に分ける。

## グラレコ構図案

- 左: handoff、吹き出しや読み込み指示のある文書
- 中央: miku-text-bundleのモード切替スイッチ
- 右: 中立なknowledge-001/002と、別枠のknowledge-index
- みくく: 右下で静かに資料を棚へ置く姿。視線は登録候補へ
- 吹き出し: 「会話の言葉を、そっと外します」

## 正確性メモ

- mode省略時はhandoff。
- knowledge-index.mdは登録対象ではなく管理用。
- ツールの責任範囲は登録候補Markdownの生成まで。

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
