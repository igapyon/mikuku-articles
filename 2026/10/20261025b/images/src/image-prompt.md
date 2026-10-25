# PHP2Shellの仕組み — Image Generation Prompt

Use case: infographic-diagram
Asset type: representative graphic-recording image for a Japanese technical article.
Create one finished, high-resolution, horizontal 3:2 Japanese educational infographic. Render the Japanese text listed below carefully and legibly. The audience is engineers reading a gentle technical essay by Mikuku.

## Style Contract

- style-profile: mikuku-graphic-recording-v1
- 横長3:2の技術グラレコ説明ポスター。Warm, clean, hand-drawn graphic recording, whiteboard explainer, delicate pen lines, restrained pastel accents. High information density with a clear hierarchy.
- Uniformly bright white to very pale ivory paper (#FFFDF5), edge to edge. fully opaque background; no transparent or semi-transparent pixels. No vignette, dark paper texture, gray-brown cast, or shadows behind lettering.
- Dark brown or almost black, high-contrast Japanese labels, including small annotations. Pastel orange, teal, and soft green belong in frames and arrows, not in faint lettering.
- Use left, center, and right regions. The largest visual element is the article-specific two-lane process diagram. No scenic backdrop or unrelated decoration.
- Show exactly one canonical Mikuku, occupying approximately 20% of the canvas, readable as the explaining character. same character, do not redesign, preserve character identity, canonical character prompt.
- みくくに物を持たせない。Do not let Mikuku hold any objects. Natural relaxed empty hands at the lower frame edge; no pointing tool, pen, notebook, or clipboard.
- Include exactly one speech bubble with the specified Mikuku sentence. Keep her presence and the bubble clear and readable.

## Article-specific Design

- layout-family: flow
- primary-relation: 中断後に残る未完成のデータと古い参照を、2本の異なる処理の流れで並べる
- The title, across the top in large clean handwritten-style Japanese, is exactly: 「PHP2Shellの仕組み」.
- Beneath the title, a smaller subtitle: 「処理が止まったあと、何が残る？」.

### Left and center: the largest diagram

Occupy roughly the left three quarters of the image with two spacious, parallel horizontal process lanes. Keep arrows unambiguous. This is a process diagram, not a row of unrelated topic cards. Preserve the difference between the two vulnerability paths.

At the top of the diagram, a narrow common-context strip has two short labels: 「PHPワーカーは続く」 / 「データは入れ替わる」. A subtle continuous outline represents the worker, with small replaceable memory blocks inside. This is supporting context, not a third vulnerability.

Upper lane, pale orange accents:
- Heading: 「① 作りかけのデータ」
- Identifier beneath the heading: 「CVE-2026-109618」
- Three left-to-right stages: 「初期化」 → 「メモリ不足で中断」 → 「未完成のデータ」.
- At the final stage, a short caption: 「終了処理が使用」.
- Use a partially filled memory/data block and an interrupted initialization arrow. This path reaches the shutdown processing of the same request. Do not draw a next-request boundary in this upper lane.

Lower lane, teal accents:
- Heading: 「② 残った古い参照」
- Identifier beneath the heading: 「CVE-2026-109619」
- Three left-to-right stages: 「データを解放」 → 「古い参照が残る」 → 「次のリクエスト」.
- At the final stage, show the old reference reaching the freed memory location, with the clear key label 「解放後使用」 and small annotation 「通常の初期化より前」.
- Draw a request boundary before 「次のリクエスト」, only in this lower lane.
- A small supporting diagram beneath this lane shows the same memory location receiving a different data block, with the short label 「別データへ再利用」. An old pointer still points there; its assumed old structure differs from the new block. This explains the memory-lifetime mismatch without exploit instructions.

### Right: consequence and Mikuku

Connect the endpoints of both lanes to a small shared consequence box, without merging their causes. Exact wording: 「条件がそろうとコード実行」.
Two short dark, legible notes beneath it: 「成立条件は環境で異なる」 / 「実行権限はWebワーカー」. These conditions are essential; do not change this into a claim that every memory error always gives code execution.

Mikuku occupies the right lower portion, with a gentle, slightly worried expression and a modest blush, looking left toward the process diagram. Use the same long chestnut twin-tails, warm brown eyes, black ribbons with deep-red trim, face shape, and overall identity described below. A simple white collared blouse matches the inspected canonical portrait. Keep the paper behind her just as uniformly bright as the rest of the poster. Her hair and clothing must not obscure the diagram or the fix strip.

Place one comfortably sized speech bubble above her, with the exact text:
「あの…終わったあとに、何が残るかが大事なのですね。」
Use natural line breaks. The wording is gentle and restrained, as Mikuku explaining the article to the reader. Do not add unrelated catchphrases or extra speech bubbles.

### Bottom: the fixes

A pale green strip across the bottom left and center, with heading 「修正の要点」. Three clear short items with simple check marks:
1. 「安全な地点で止める」
2. 「さらに高い上限では終了」
3. 「内部状態のリセット」
The third means clearing internal state so old references do not carry into the next request. Do not depict terminating every worker after every request.

### Accuracy and text policy

- Preserve the title, all ten source keywords (PHP2Shell, PHPワーカー, メモリ不足, 未完成のデータ, 古い参照, 次のリクエスト, 解放後使用, コード実行, 安全な地点, 内部状態のリセット), both exact CVE identifiers, the process relationships, and the speech bubble.
- Use only the facts and labels specified here. Do not add patch version numbers, scores, worldwide incident statistics, model names, code snippets, commands, brand logos, or claims about a tested environment.
- The first vulnerability is incomplete data used by shutdown processing. The second carries a dangling reference across requests. Do not turn them into one identical use-after-free path.
- Do not print layout metadata, file paths, this prompt's instructions, the words layout-family / primary-relation, or the accuracy notes on the poster.
- No skulls, hooded attackers, dramatic red scenes, unrelated scenery, extra mascots, corporate slide layout, or photorealistic elements.

## Deviation Record

none

## Mikuku Canonical Character Prompt

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

For this diagram only, turn her face and gaze toward the diagrams on her left, while preserving every identity feature above. This allowed pose adjustment overrides only the canonical gaze direction. Her lighting must not darken the uniformly bright infographic background.
