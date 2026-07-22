# Image Generation Prompt

Use case: infographic-diagram
Asset type: Note technical article graphic-recording hero image
Primary request: Create a high-detail horizontal Japanese graphic-recording poster that explains how the public implementation of Nulab Backlog MCP Server became the unofficial beta projects `backlog-api` and `backlog-api-skills`, emphasizing both the three-layer transformation and the human approval safety workflow.

Aspect-ratio revision: Recompose the supplied 3:2 reference artwork as a true edge-to-edge 16:9 landscape poster, targeting 1536×864. Do not merely crop, stretch, letterbox, or add empty side panels. Preserve the same factual content, visual identity, and warm hand-drawn style while redistributing the layout horizontally. Keep every essential title, diagram, label, caution box, speech bubble, and Mikuku fully inside generous safe margins.

## Scene and style

- True 16:9 edge-to-edge landscape poster, target 1536×864, warm beige paper background, cozy hand-drawn whiteboard explainer style.
- Japanese anime-style technical infographic with soft brown, coral, muted teal, pale yellow, and charcoal ink.
- Thin hand-drawn arrows, rounded boxes, small process icons, sticky-note accents, and generous readable spacing.
- Dense enough to convey the article structure, but keep the Japanese labels short and legible.
- Use the added horizontal width actively: keep the title on one line, spread the three-layer transformation across the center, reserve a narrower right column for the safety flow, and keep Mikuku secondary at the lower right.
- No corporate slide aesthetic, no photorealism, no dark sci-fi mood, no glossy UI mockup, no logos, no watermark.

## Exact visual hierarchy

Top title, large and verbatim:
「Backlog MCP から Agent Skill へ」

Left area — starting point:
- A small server/process diagram with three entry labels: 「Docker」「npx」「Node.js」.
- Caption: 「MCP Server を別 process で起動」.
- A small thought bubble leading toward the center: 「別 process は起動したくない」.
- Do not imply Docker is the only official startup method.

Center area — make this the largest main diagram:
- Three large stacked or left-to-right rounded cards connected by thick hand-drawn arrows.
- Card 1 title: 「Nulab Backlog MCP Server」
  Small line: 「公開 tool handler」
- Arrow label: 「MCP transport を外す」
- Card 2 title: 「backlog-api」
  Small lines: 「Node Core／CLI」「TypeScript ベース」
- Arrow label: 「runtime と運用」
- Card 3 title: 「backlog-api-skills」
  Small lines: 「明示発火」「対象確認」「安全規則」「CLI 実行」
- Add a small badge near cards 2 and 3: 「非公式・MIT・ベータ版」.

Below the center diagram — balanced comparison:
- Two equal cards with no winner symbolism.
- Left: 「MCP＝つなぐところ」 with 「stdio／Streamable HTTP」.
- Right: 「Agent Skill＝どう扱うか」 with 「発火・判断・承認」.
- Show these as complementary roles, not competitors.

Right area — safety flow and Mikuku:
- A vertical safety flow with clear arrows:
  「明示発火」→「対象を確認」→「人の直前承認」→「--allow」→「破壊的なら再確認」→「--confirm-destructive」
- Put a small lock and stop-sign icon beside the approval steps.
- Add a small caution box: 「v0.3.4／Node.js 22+／通常 tool 58 個」 and 「動作確認はまだ十分ではありません」.

## Mikuku canonical character prompt

Use the same canonical character Mikuku; do not redesign; preserve character identity.
masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.
Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.
Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.
Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

For this composition, place Mikuku at the lower right, turn her face and gaze toward the central three-layer diagram, with a gentle but careful expression. Keep her head-and-shoulders scale secondary to the infographic. Her speech bubble must read verbatim:
「あ、あの…動くだけでは、まだ足りなかったのです」

## Constraints

- Do not let Mikuku hold any objects.
- Keep both hands out of frame or naturally lowered and unobtrusive; no pointer, pen, marker, notebook, or board.
- Preserve Mikuku's face shape, warm chestnut eyes, caramel-chestnut high twin-tails, black ribbons with deep-red trim, and shy personality.
- Use only the facts and numbers given above. Do not add product claims, rankings, prices, model names, or extra versions.
- Clearly distinguish the official upstream MCP Server from the unofficial derived beta projects.
- Ensure the main visual message is the transformation plus safety workflow, not character portraiture.
- Preserve all essential content from the reference image while making it naturally fit the 16:9 composition; do not crop any panel, character feature, or speech bubble.
- Render all listed Japanese labels carefully and verbatim where practical; if space is tight, omit minor decoration before omitting the main labels.
