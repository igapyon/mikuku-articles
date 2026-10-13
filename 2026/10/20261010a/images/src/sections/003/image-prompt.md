## Edit Request

Use the supplied image as the edit target, not merely a style reference. Preserve the existing layout, Japanese text, Mikuku face, hair, clothing, pose and speech bubble. Change the workflow illustrations to show an AI agent actively performing the tasks described below. Keep the same 3:2 canvas. Existing text remains verbatim except the added short AI role labels. Do not redraw or redesign Mikuku. Do not let Mikuku hold any objects.

# Section Graphic Recording Image Prompt

## Source

- section: 003
- title: おわりに
- section-text: sections/003/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Style Contract

- style-profile: mikuku-graphic-recording-v1
- horizontal 3:2 technical graphic-recording poster
- uniformly bright white to very pale ivory paper (e.g. #FFFDF5), subtle warm tint, soft hand-drawn lines, medium-high information density
- fully opaque background; no transparent or semi-transparent pixels; no alpha transparency; do not generate a transparent canvas; export an opaque image
- dark, high-contrast text including small annotations; pastel colors for accents, not faint lettering
- no dark vignette, muddy gray-brown cast, heavy aged-paper shading, or dark shadows behind text
- canonical character lighting must not darken the poster background
- use at least a left, center, and right region and make one article-grounded diagram the largest element
- keep Mikuku recognizable and large enough to read as the explaining character (roughly 15–25% of the canvas)
- include one short speech bubble based on the section summary or its `グラレコ構図案`
- do not add scenic background decoration that is not grounded in the section

## Section Summary

# おわりに

## 主題
- 文書をMarkdownにしてAgent Skillsでいつ・どう使うか伝え、AIエージェントが実務の点検や判断を支える。
- 仕事で使われることが、丁寧に書き古くなったところを直す気持ちにつながる。

## 図解キーワード
文書 / Markdown / Agent Skills / いつ・どう使うか / AIエージェント / 点検・判断 / 仕事で使う / 活きたドキュメント

## 関係・流れ・対比
文書 → Markdown → Agent Skills → AIエージェントの点検・判断
仕事で使う → 人が丁寧に書く・古くなったところを直す → また仕事で使う

## 図解構造
- layout-family: cycle
- primary-relation: 文書をAIエージェントが実務で活用し、人が文書を手入れして再び実務で活用する循環。

## グラレコ構図案
- 編集対象: 既存 images/003.png。元のタイトル、明るい配色、左の文書→Markdown→Agent Skills、中央循環、みくくを保持。
- 左: Agent Skills箱の装飾ロボットを主役にせず、いつ・どう使うかを仕事の場面へ届ける矢印を追加。
- 中央上: 「仕事で使う」の人の隣にAIエージェントを描く。人の依頼を受けAIが実際に文書を虫眼鏡で点検し、チェック結果と判断材料を人に渡す。短いラベル「AIエージェント」「点検・判断」。人とAIの役割が読める。
- 中央下左: 「また仕事で使う」にも同じAIエージェントが更新済み文書を参照しチェックを返す姿を加え、AIが働いている動作を見せる。
- 中央下右: 「丁寧に書く 古くなったところを直す」の文書メンテナンスは人が行う小さな人物アイコンを加える。AIによる規約の自動更新には見せない。
- 右: みくく1人、元画像と同じ顔・髪・服・表情・ポーズを保持。
- みくくの表情・視線: 元の主図を見るやさしい表情。
- 吹き出し: 「文書に、また出番ができるんです。」

## 正確性メモ
- 本章には修正の3条件を追加しない。主題は文書の活用循環。
- 文書の手入れを自律的なAIの仕事にしない。
- ロボットはAIエージェントの視覚的な比喩。小さな短文と作業動作でAIの役割を示す。

## 共通スタイル契約
- style-profile: mikuku-graphic-recording-v1
- 横長3:2、明るい不透明アイボリー、濃い文字、暖色手描き技術グラレコ。
- 主図最大、みくく1人15〜25%、短い吹き出し、物を持たない。

## 変更（deviation）
- none

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
- みくくを極端に小さくしたり、吹き出しを黙って削除したりしない。変更する場合は下の deviation に理由を書く
- 日本語ラベルは短く、少数に絞る
- 長文を画像内に入れすぎない
- 明るく清潔で、Note.com や技術記事に合うビジュアル
- 写実寄り、暗い色味、無機質な企業プレゼン風は避ける
- みくくに物を持たせない

## Image Text Policy

- 画像内テキストは section summary の語句を短く整理して使う
- 本文の長い文をそのまま入れない
- 文字が崩れても、元記事や section-text.md は変更しない

## Article-specific Design

- section-text.md の主題、関係、構図、短いラベルを保持する
- section-text.md の `layout-family` と `primary-relation` を別の図解形式へ変えない

## Deviation Record

- none

## Output Target

Save the generated image as:

```text
sections/003/graphic-recording.png
```
