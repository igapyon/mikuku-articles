# Image Generation Prompt

Use case: infographic-diagram
Asset type: a whole-article graphic-recording poster for a Japanese technical article

Create one polished, high-resolution, wide 16:9 Japanese graphic-recording poster. It should look like a warm hand-drawn whiteboard explanation on light beige paper: soft brown and pastel accent lines, clear arrows, rounded boxes, small technical icons, generous whitespace, and readable visual hierarchy. Information-rich but not crowded. Cozy Japanese anime technical explainer style, not a corporate slide.

## Exact visual theme

Main theme: 「Shift_JIS を壊さず AI agent に渡す『小さな橋』」

The largest central visual is a small, careful bridge connecting an AI agent on the left to legacy Windows-31J Java/JSP text files on the right.

### Left area: the problem

- Show a compact flow labeled 「UTF-8 前提の道具」 pointing toward Java/JSP files.
- Add a warning burst labeled 「文字化け」 and a few broken Japanese glyph-like marks.
- Add the short qualifier 「ある特定の agent ハーネス」 so the image does not claim that every AI agent has this problem.
- Mood: concern and risk, but not horror or disaster.

### Center area: the small bridge

- Draw a two-layer bridge.
- Upper entrance layer label: 「Agent Skill = 入口」
- Lower structural layer label: 「CLI = 文字コード処理」
- Across the bridge, show one continuous directional flow with these exact labels:
  「search → read → update → verify」
- Beside that flow, add a small ribbon label: 「最後まで同じ経路」
- Show a small revision token moving from read to update, labeled 「revision」
- Add three compact safety badges around the bridge:
  「文字コードを維持」
  「BOM・改行を維持」
  「途中で変わったら止まる」

### Right area: protected files

- Show clean document icons labeled 「Java」 and 「JSP」 with a small label 「Windows-31J」
- Place a soft shield around them.
- Add a small repository rule card labeled 「repository rule」
- Add a small beta tag: 「v0.5.0 / ベータ版」
- Add a quiet future note: 「ハーネスが育てば、役目を終えるかも」

### Small development note

Near the lower center, include a modest supporting card, clearly secondary to the bridge:
「GPT-5.6 Sol Ultra と対話」
「繊細な仕様を整理 → test で固定 → 完成へ」

## Mikuku character

Place Mikuku on the right edge, head-and-shoulders or upper-body, facing left and looking at the central bridge. She is slightly worried but relieved, gently explaining the diagram. She holds no objects; keep hands naturally lowered or outside the frame.

Canonical character prompt, preserve identity exactly; same character, do not redesign, preserve character identity:

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her left and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

Mikuku speech bubble, render verbatim:
「あ、あの…最後まで同じ入口を使うのです…！」

## Text and typography

- Render all quoted Japanese text verbatim and legibly.
- Use friendly handwritten Japanese lettering with clear character forms.
- Do not add paragraphs of prose.
- Do not invent additional model names, test counts, dates, prices, ratings, or product capabilities.
- Keep the main hierarchy visually obvious: problem → small bridge → protected files.

## Constraints

- The article concerns a specific AI agent harness; do not depict all AI agents as universally broken.
- Treat Shift_JIS as the familiar umbrella wording and Windows-31J as the concrete file encoding; do not present them as two unrelated competing encodings.
- The dedicated path applies only to encoding-sensitive files, not every UTF-8 file.
- Keep the beta and potentially temporary nature visible but secondary.
- Do not let Mikuku hold any objects.
- No pens, pointers, boards, notebooks, or devices in Mikuku's hands.
- No malformed or extra fingers.
- No photorealism, dark cyberpunk, strong science-fiction styling, sterile corporate presentation, watermark, or unrelated mascot.
