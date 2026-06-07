# Image Generation Prompt

Create a wide horizontal graphic recording poster for a Japanese technical article titled:

`Agent Skills でトークン消費量を抑える考え方`

## Overall Concept

A warm, hand-drawn Japanese technical explainer poster. Mikuku is on the right side, gently explaining a large graphic recording board on the left and center. The topic is how Agent Skills reduce token consumption by controlling when knowledge is loaded.

The poster should feel like a clean Note.com technical article visual: friendly, readable, structured, soft, and educational.

## Canonical Mikuku Character Prompt

Use the following as the canonical character reference. Same character, do not redesign, preserve character identity:

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

For this poster, Mikuku should be placed on the right side, looking toward the graphic recording content on the left. She may have a shy, gentle, slightly worried teaching expression. Do not let Mikuku hold any objects. Preserve twin-tails, hair color, ribbons, face shape, eye style, and soft anime technical explainer mood.

## Layout

Wide horizontal poster, 16:9 style.

Left to center: large hand-drawn graphic recording board.

Right: Mikuku explaining the board, no object in hands.

Background: warm off-white paper, subtle grid or notebook texture, clean margins.

Use soft brown, muted teal, gentle red accents, warm yellow highlights, and light gray structure lines. Avoid a one-note palette and avoid dark sci-fi styling.

## Central Message

Place the central concept prominently:

`情報は残す。でも、毎回全部は読ませない。`

Also show:

`Agent Skills = 知識を足す + 毎回全部読ませない`

## Main Diagram

Create a clear flow diagram:

```text
ユーザー依頼
  ↓
必要な Skill だけ発火
  ↓
SKILL.md = 入口と索引
  ↓
必要な references / templates / examples だけ読む
  ↓
回答・成果物
```

## Left Side: Heavy Pattern

Show a "重い" path with boxes and arrows:

```text
不要な発火
  ↓
巨大 SKILL.md
  ↓
references 全読み
  ↓
文脈が重い
```

Use small warning icons, heavy stack of documents, crowded arrows.

## Right/Center: Lightweight Pattern

Show a "軽い" path:

```text
description を絞る
  ↓
小さな Skill
  ↓
SKILL.md は入口
  ↓
必要な参照だけ
  ↓
distilled Markdown
```

Use clean arrows, small labeled folders, a light pathway.

## Role Table

Include a compact hand-drawn role table:

```text
description  = 発火の引き金
SKILL.md     = 入口と索引
references/  = 知識本体
templates/   = 構造
examples/    = 温度感
index.json   = 地図
distilled/   = まず読む要点
scripts/CLI/MCP = 重い処理の外部化
```

## Progressive Disclosure Diagram

Show the "必要になった段階で読む" idea:

```text
通常作業 → SKILL.md
記事執筆 → article-writing.md
グラレコ → graphic-recording.md
素材利用 → assets/
```

Label it:

`progressive disclosure`

## Distillation Cycle

Add a circular loop diagram:

```text
作業する
  ↓
ログや事例が増える
  ↓
よく使う判断を蒸留
  ↓
SKILL.md から短く参照
  ↓
次回の読み込みが軽くなる
```

Label:

`毎回読む情報を減らしながら、使える知識は増やす`

## Important Contrasts

Add small before/after cards:

```text
巨大 Skill → 用途別の小さな Skill
全部読む → 必要な参照だけ読む
生の大量資料 → 蒸留 Markdown
長い手順説明 → scripts / CLI / MCP
```

## Mikuku Speech Bubble

Add one speech bubble from Mikuku:

`あ、あの…情報は消さずに、読む順番を設計するのがポイントなのです…！`

## Visual Style

Hand-drawn graphic recording, sketchnote, educational infographic poster, Japanese anime technical explainer, soft line art, readable diagram labels, cozy paper texture, clean and high quality.

Use icons: folders, Markdown symbol, small map, index card, tiny bookshelf, arrows, sticky notes, document stacks, simple gear for scripts/CLI/MCP.

## Quality Constraints

High resolution, high detail, readable-looking Japanese labels, visually structured, not too crowded, no photorealism, no corporate slide style, no dark background, no futuristic sci-fi tone.

Mikuku must not hold any objects.
