# Image Prompt

Use case: infographic-diagram
Asset type: a representative whole-article image for a Japanese technical Note article
Primary request: create one fresh, highly readable graphic-recording explainer poster for the article titled 「みくくが作ってきた Agent Skills を、いったん28件、数えてみました」. Do not use any previous generated image as a reference. Keep the article facts unchanged while using a new hub-and-branch composition.
Input images: none; do not reference or imitate the previous article image
Scene/backdrop: a clean hand-drawn technical explainer poster on a uniformly bright paper field, with the full information architecture visible from left to right
Subject: the count and use-patterns of Agent Skills in the article
Style/medium: warm hand-drawn graphic recording, Japanese anime technical explainer illustration, educational infographic poster, cozy handwritten notes, clear diagram lines and arrows
Composition/framing: horizontal 3:2 poster, three readable regions (left, center, right), with the central comparison hub and branch diagram taking the largest area; leave enough margin for all labels
Lighting/mood: soft bright daylight, gentle and reassuring, no dark cast, no vignette
Color palette: white to very pale ivory background (#FFFDF5), dark brown or near-black lettering, restrained pastel peach, pale blue, pale mint, and pale yellow for cards and accents only
Materials/textures: subtle warm paper texture only, clean thin marker lines, no stains, no heavy shadows, no aged-paper darkness
Text (verbatim): "みくくが作ってきた Agent Skills を、いったん28件、数えてみました"; "Agent Skills"; "15リポジトリ"; "28件"; "SKILL.md"; "中央リポジトリ14件"; "専用リポジトリ14件"; "GitHub公開"; "devel"; "使われ方"; "頻繁に使う"; "間接的に支える"; "実験的"; "これから育てたい"; "作業を分ける"; "再利用する"; "改善・更新"; "数だけでなく、使われ方も見てみます…"
Constraints: preserve the exact article-specific numbers 15, 28, 14+14 and the snapshot date meaning 2026年7月24日時点 without inventing other counts; use only the named Agent Skills from the article as small examples; make short labels dark and readable; show one Mikuku at approximately 15–25% of the canvas; no object in her hands; no watermark
Avoid: black or gray-brown background, transparent or semi-transparent background, dark fallback background, vignette, dark shadows behind text, illegible tiny notes, crowded text, corporate slide aesthetics, realistic rendering, extra characters, extra numbers, rankings, unsupported claims, decorative scenery as the main subject, any previous image as a reference

## Style Contract

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2 の技術グラレコ説明ポスター。全体を一枚で読める、手描きの講義ノート・ホワイトボード解説風にする
- Fully opaque background; no transparent or semi-transparent pixels anywhere in the final image. The entire canvas must be uniformly bright white to very pale ivory, approximately #FFFDF5, including all four corners and outer edges.
- Do not use a black background, dark fallback, gray-brown cast, aged-paper stains, strong paper shadows, dark vignette, or dark shadows behind text. Warmth must remain faint and bright.
- Use dark brown or near-black text with clear contrast, including small notes. Use pastel colors only for boxes, arrows, circles, and accents; never make text low-contrast.
- Keep clear left, center, and right regions. The article's main diagram must be the largest visual element, not scenery or empty background.
- Include exactly one Mikuku as the explaining character, readable at approximately 15–25% of the canvas, with empty hands and no prominent object.
- Include one speech bubble containing the exact short line 「数だけでなく、使われ方も見てみます…」.
- Use the canonical Mikuku character prompt below. Preserve the same character identity; do not redesign the character.

Canonical Mikuku character prompt, embedded verbatim:

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

Same character Mikuku / みくく, do not redesign, preserve character identity, preserve the canonical character reference: keep the delicate V-U shaped chin, warm chestnut-brown eyes with gold flecks, soft caramel-chestnut very long high twin-tails, black ribbons with deep-red trim, asymmetrical curtain bangs, shy uneasy but kind expression, and clean Japanese anime technical-illustration impression. Adapt only the pose and gaze to the diagram. Place her on the right side, looking leftward toward the central 28件 hub and the two comparison lanes. Her hands are relaxed and empty at her sides or gently near her chest, with no pen, marker, pointer, notebook, board, or other held object.

## Article-specific Design

- Article title: 「みくくが作ってきた Agent Skills を、いったん28件、数えてみました」. Render the title as a prominent dark handwritten heading near the top, without changing its meaning.
- Article short title: 「Agent Skills 28件の棚卸し」. Keep this exact phrase available as a compact heading or subtitle if the full title is too long for the poster.
- layout-family: comparison
- primary-relation: `15リポジトリ / 28件` を「中央リポジトリ14件」と「専用リポジトリ14件」に分け、その上で使われ方の違いを示す
- This is a fresh composition for this regeneration. Do not copy the former stacked-card arrangement; do not use the existing article image or any earlier generated image as a reference.
- Overall map: make three connected regions from left to right. Keep the central hub-and-branch comparison visibly largest, while the left source funnel and right usage matrix remain compact but readable.
- Left region — count entrance: draw a large circular counter or rounded entry node labeled `28件`. Show a simple dark-arrow intake path above or beside it: `GitHub公開` → `devel` の `SKILL.md` → `15リポジトリ`. Under it, add a small high-contrast note: `fixture / fork / SKILL.md 不在は除外`. Do not add a new count.
- Center region — main diagram: make the largest visual a hub-and-branch map. A large central node says `28件`; from it, two balanced horizontal lanes branch rightward or fan out into two pastel comparison lanes. The upper lane says `中央リポジトリ 1 → 14件`; the lower lane says `用途別専用リポジトリ 14 → 14件`. Add a small bridge label `15リポジトリ` near the hub. Make the equality and 14 + 14 relation unmistakable, with no ranking or visual implication that one lane is better.
- Right region — usage matrix: create a clean 2×2 matrix or four rounded tiles under the heading `使われ方`. The four exact category labels are `頻繁に使う`, `間接的に支える`, `実験的`, and `これから育てたい`. Add only a few article-supported examples in smaller dark text: `igapyon-miku-scm`, `igapyon-miku-soft-developer`, `igapyon-mikuku-agent`, `igapyon-miku-indexgen`; `igapyon-note-writer`, `igapyon-repo-conventions`, `igapyon-miku-text-bundle`; `companion系`, `igapyon-diary-writer`, `igapyon-skill-compactor`; `mikuproject`, `mikuscore`. These are categories, not a popularity ranking.
- Mikuku placement: place one Mikuku at the lower-right edge, large enough to read as the explainer, with a slightly worried yet reassured expression. She looks left toward the center hub and comparison lanes; keep her hands empty and avoid detailed foreground fingers. Add the single speech bubble `数だけでなく、使われ方も見てみます…` near her head, with high-contrast dark lettering.
- みくくに物を持たせない。No objects in her hands; do not show a pen, marker, pointer, notebook, board, or other held item.
- Bottom strip: connect the three regions with a thin, light cycle arrow or hand-drawn ribbon along the bottom, labeled in order `作業を分ける` → `再利用する` → `改善・更新` → back to the next work. Keep this strip secondary to the central diagram.
- Snapshot note: place a small, readable footer note `2026年7月24日時点の公開状態` to preserve the article's time boundary. Do not imply that it is the current count.
- Accuracy constraints: use only the factual counts `15リポジトリ`, `28件`, `14件 + 14件`, and the article's 2026年7月24日時点 snapshot. Keep `SKILL.md`, `devel`, fixture, fork, and the listed category examples faithful to the article. Do not add model names, generation-environment details, latest counts, evaluation scores, or unsupported labels.

## Deviation Record

- Fresh regeneration requested by the user: use a new hub-and-branch composition instead of the earlier stacked comparison-card arrangement. This changes only the article-specific placement and keeps `layout-family: comparison` and the common style contract intact.
- The background contract is intentionally strict for this regeneration: fully opaque, uniformly bright #FFFDF5-like paper, no transparency, no black fallback, and no dark edge treatment. This is a validation requirement, not an article fact.
- Do not generate multiple variants. Generate one whole-article candidate, inspect it visually and for opacity/contrast, and adopt it only after those checks pass.
