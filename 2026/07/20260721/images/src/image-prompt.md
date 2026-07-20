# Image Generation Prompt

Create one high-resolution, wide 16:9 Japanese graphic-recording poster for a technical Note.com article. The poster explains `miku-ai-assistant-builder-skills v0.8.0`, a small Agent Skill that prepares many source files for registration as AI-assistant Knowledge.

## Visual style

- Cozy hand-drawn graphic recording, educational infographic poster, Japanese technical explainer
- Warm ivory and beige paper background, soft brown linework, pastel teal, muted orange, pale red accents
- Whiteboard lecture-note feeling, with arrows, rounded boxes, folder and document icons
- Dense enough to explain the whole article, but maintain clear hierarchy and generous whitespace
- Clean, friendly, precise, not corporate, not photorealistic, not dark, not futuristic
- Use short, legible Japanese labels. Do not invent extra claims

## Main title

At the top, clearly write:

「たくさんの資料を AI アシスタントへ渡す、その少し手前」

Small subtitle:

「miku-ai-assistant-builder-skills v0.8.0」

## Main composition

Use three visual regions from left to right.

### Left: inputs

Show many small scattered document cards labeled:

- 「Markdown」
- 「Code」
- 「Memo」

Below them, show a separate carefully prepared group labeled:

- 「人が準備した資料」
- 「Word」
- 「Excel」
- 「PowerPoint」

Visually communicate the problem with a small warning card:

- 「ファイル数が多い」
- 「そのままでは登録しにくい」

### Center: the largest main diagram

Draw a large two-lane preparation pipeline.

Upper lane:

「多数のテキスト」 → 「miku-text-bundle」 → 「少数の Knowledge」

Lower lane:

「人が準備」 → 「manual-input/」

Merge the two lanes into:

「Markdown」 → bridge arrow labeled 「miku-md2docx」 → 「DOCX」

Then place a clean folder labeled:

「upload/」

Add a small two-step inset nearby:

「第 1 段階：対象を決めて、いったん停止」
↓
「人が追加／追加なしを確認」
↓
「第 2 段階：まとめて、変換して、整える」

The central message, visually emphasized in a rounded banner:

「バンドルする。DOCX へ橋渡しする。設定内容まで整える。」

### Right: destinations and human boundary

Show two destination cards:

- 「Microsoft 365 Copilot Agent Builder」 with a DOCX icon
- 「Google Gemini Gem Classic」 with Markdown and DOCX icons

Immediately before the destination cards, show a human check gate with a checkmark and label:

「人が確認して登録」

Add a small boundary card:

- 「自動アップロードしない」
- 「共有まで行わない」
- 「小さな責務を保つ」

Add one concise caution box:

「登録できた ＝ 全内容を毎回参照、ではない」

Add another small environment note:

「ファイル添付できるライセンス・利用環境が必要」

## Mikuku character — canonical character prompt

The same canonical character Mikuku appears at the lower right, occupying about 22% of the canvas, looking left and slightly upward toward the central pipeline. Preserve character identity; do not redesign her.

Canonical character description:

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

Adapt only her gaze direction so she naturally looks toward the diagram on her left. Keep the same face shape, eyes, hair color, twin-tails, ribbons, and gentle reserved personality. Same character, do not redesign, preserve character identity, canonical character reference.

Mikuku must not hold any objects. Keep both hands simple, relaxed, and mostly outside the crop or naturally resting. Do not draw a pen, pointer, marker, board, notebook, or tool in her hands.

Her speech bubble must say exactly:

「あ、あの…資料が入口で迷子にならないように、少し手前を整えます」

## Accuracy constraints

- This is a beta Agent Skill for preparing deployment data, not an AI assistant that creates, uploads, or shares agents automatically
- For Agent Builder, represent the key issue as many files and Markdown-to-DOCX conversion; do not display disputed file-size figures
- If showing the number limit, write only 「埋め込みファイル 最大 20 件」 next to Agent Builder
- Do not state a fixed file-count limit for Gem Classic
- Do not imply that all registered content is always searched or referenced
- Do not depict internal retrieval architecture or summary-search behavior as an official mechanism
- Do not add pricing, model names, rankings, release history, or unsupported features

## Avoid

- Photorealism
- Dark sci-fi atmosphere
- Generic corporate slide design
- Tiny unreadable paragraphs
- Excessive decorative text
- Character redesign
- Different hair color or hairstyle
- Objects in Mikuku's hands
- Extra fingers, duplicated hands, malformed anatomy
- Logos that imitate official brand marks; use clean text cards instead
