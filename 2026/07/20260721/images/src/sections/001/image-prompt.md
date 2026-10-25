# Section Graphic Recording Image Prompt

## Source

- section: 001
- title: はじめに
- section-text: sections/001/section-text.md
- mikuku-prompt: /Users/igapyon/.codex/skills/igapyon-mikuku-agent/assets/mikuku/mikuku-portrait-short-prompt.md

## Task

Create a horizontal Japanese graphic recording explainer image for this section.
Use only the section summary below as the explanation source. Do not mix in other article sections.

## Section Summary

# はじめに

## 主題

- たくさんの資料を AI アシスタントへ渡す「少し手前」を整える小さな準備係。
- 開発中の `miku-ai-assistant-builder-skills` v0.8.0 を簡潔に紹介する。
- 多数の資料を登録可能な件数へまとめ、渡しやすい形にするベータ版。

## 図解キーワード

- たくさんの資料
- AI アシスタント
- 登録前の準備
- v0.8.0
- 小さな準備係

## 関係・流れ・対比

多数の資料 → 登録前の準備 → 渡しやすい形 → AI アシスタント

## グラレコ構図案

- 左: Markdown やメモなど多数の小さなファイル群。
- 中央: 「登録前の準備」と書いた整理工程。
- 右: Agent Builder と Gem Classic を示す二つの受け皿。
- みくくの表情・視線: 中央の整理工程を見ながら、少し緊張しつつ丁寧に説明する。
- 吹き出し: 「その少し手前を整えます」

## 正確性メモ

- Agent Skill は AI アシスタント自体を自動作成しない。
- v0.8.0 はベータ版として紹介する。
- 記事本文に明記された事実だけを使い、未記載の数値を加えない。

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
sections/001/graphic-recording.png
```
