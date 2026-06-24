# Section Graphic Recording Image Prompt

## Source

- section: 011
- title: いまのところの整理
- section-text: sections/011/section-text.md
- mikuku-prompt: /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# 011 いまのところの整理

## 主題

- `igapyon-agent-state-management` の現時点の整理
- Markdown 外部化、Setup/Resume、既存 TODO 保護、4ファイル運用
- 小さな運用をひとつずつ外に出す

## Skill の特徴

- AIエージェント作業の状態を Markdown に外部化
- 新規セットアップと作業再開を分ける
- 既存 `TODO.md` を壊さない
- `GOAL.md` / `TODO.md` / `DECISIONS.md` / `HANDOFF.md` を軽く保つ
- 長い運用プロンプトを毎回貼らない

## 自然な順番

```text
状態ファイルを考える
  ↓
AIエージェントがどう扱うかを Skill にする
  ↓
実際のリポジトリで使う
  ↓
足りないところを調整する
```

## グラレコ構図

- 5つの特徴をチェックリストとして配置
- 下部に「小さな運用を外に出す」階段
- みくく: 「大きな仕組みより、小さく外に出す方が続けやすそうです…」

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
