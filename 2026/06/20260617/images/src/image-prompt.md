# Image Generation Prompt

Create a wide horizontal graphic recording poster for a Japanese technical essay titled:

「簡易RAG風Agent Skillsの作成 step2：miku-indexgenを足す」

## Character: Mikuku / みくく

Use the following as the canonical character prompt. Same character, do not redesign, preserve character identity, canonical character reference.

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

Do not let Mikuku hold any objects. Place Mikuku on the right side, looking gently toward the diagrams on the left and center. She has a shy, kind, slightly worried expression and explains the topic with a speech bubble.

## Overall Visual Style

Wide horizontal poster, Japanese anime-style technical explainer, hand-drawn graphic recording, whiteboard lecture note style, clean and readable, warm paper background, soft brown and pastel accent colors, thin clean line art, soft cel shading, cozy educational tech poster. Use arrows, boxes, folder icons, Markdown icons, small index-card icons, map icons, simple charts, and speech bubbles.

Avoid photorealism, dark sci-fi mood, corporate slide style, overly flat UI, extreme text density, unreadable tiny text, or Mikuku holding a pen, pointer, notebook, board, or any object.

## Poster Layout

Left and center: the graphic recording explanation.
Right: Mikuku explaining.

Use large Japanese headings that are visually readable:

1. 「step2: index.json を足す」
2. 「raw = 本文 / index = 地図」
3. 「まず索引 → 候補 → 本文」
4. 「同じプロンプトで比較」
5. 「探索の入口が変わる」

## Content to Draw

### Main Flow Diagram

Draw a central flow:

ユーザー依頼
↓
SKILL.md
↓
index.json
↓
候補 Markdown
↓
本文を読む
↓
回答整理

Make `index.json` look like a small map or catalog card.

### Before / After Comparison

Two side-by-side panels:

Before: 「index なし」
- wide raw corpus folder
- agent looking for files directly
- label: 「広い棚を直接探す」
- small note: 「探索が揺れやすい」

After: 「index あり」
- index card first
- arrows to selected Markdown files
- label: 「目録を見る → 必要な本文へ」
- small note: 「入口が安定」

### Role Split

Draw a compact table or four labeled boxes:

- `SKILL.md`: 探索順の指示
- `README.md`: 復元手順
- `references/raw/`: 記事本文
- `index.json`: 軽い地図

### Token Observation

Draw a simple soft chart:

- index なし: 約 110.6K used
- index あり: 約 82.4K used
- 差分: 約 28.2K used
- note: 「ただし揺れあり」

Do not present this as a strict benchmark. Make it look like an observation note.

### Growth Cycle

Draw a small cycle:

運用 → 観察 → index 追加 → 探索安定 → 蒸留メモ → 次回安定

## Mikuku Speech Bubble

Include one speech bubble near Mikuku:

「あ、あの…index は答えではなく、本文へ向かう小さな地図なのです…！」

## Quality

High resolution, clear composition, legible Japanese headings, cozy hand-drawn infographic, bright soft light, article title image suitable for Note.com and technical blog publishing.
