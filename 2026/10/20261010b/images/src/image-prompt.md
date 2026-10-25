# Image Generation Prompt

Create one polished, information-rich Japanese graphic-recording explainer poster for the article below. Preserve every listed model name, number, price, comparison, and qualification exactly. Do not invent text or factual claims. Make Japanese labels short, large, high-contrast, and correctly spelled; use the exact quoted labels below. Landscape 3:2 canvas.

Article title: 「GPT-5.6 Lunaも衝撃価格だったのに、GPT-6ではSolもLunaもさらに安い」

## Style Contract

- style-profile: mikuku-graphic-recording-v1
- Horizontal 3:2 technical graphic-recording poster, divided into clear left, center, and right regions; make the central diagram the largest visual element.
- Uniformly bright white to very pale ivory background (#FFFDF5), fully opaque background; no transparent or semi-transparent pixels. Keep warm paper character subtle, not brown or aged.
- Dark brown or near-black lettering with strong contrast, including all small notes. Soft hand-drawn lines, hand-lettered labels, pastel accents only for outlines and arrows. No dark vignette, gray-brown color cast, dirty paper, or shadows behind text.
- A cozy Japanese anime technical explainer, like a carefully drawn whiteboard graphic-recording poster. Dense with useful information, arrows, comparison cards, number bars, and small simple icons. No unrelated scenery or decorative objects.
- Include exactly one clearly recognizable Mikuku as a presenter, large enough to read as a character (about 15–20% of canvas). Place her on the right and turn her gaze toward the central price comparison. Do not let Mikuku hold any objects.
- Include one readable speech bubble with this exact text: 「単価だけじゃなく、仕事全体の費用で見てみたいです…！」

Canonical Mikuku character prompt, same character, do not redesign, preserve character identity:

> masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.
>
> Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.
>
> Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.
>
> Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

Use the supplied Mikuku reference image for identity. Keep her face, warm chestnut-brown eyes, very long caramel-chestnut twin-tails, black ribbons with deep-red trim, bangs, and gentle shy expression consistent with that reference. She may look left toward the chart for this composition; do not change her canonical design. Keep her hands out of view or relaxed and empty.

## Article-specific Design

- layout-family: comparison
- primary-relation: トークン単価は下がったが、選ぶ基準は必要な品質で仕事を完了するまでの総費用
- Main title at top: 「GPT-5.6 Lunaも衝撃価格だったのに、GPT-6ではSolもLunaもさらに安い」
- Left region, compact price-history comparison headed 「100万トークン / Standard・短い文脈」. Keep columns 「GPT-5.6初期」, 「GPT-5.6現在」, 「GPT-6系列」. Show exact input / output pairs:
  - Astra: only GPT-6 row, 「$10 / $50」
  - Sol: 「$5 / $30」 → 「$4 / $20*」 → 「$2 / $10」
  - Terra: 「$2.50 / $15」 → 「$2 / $12」 → 「後継掲載なし」
  - Luna: 「$1 / $6」 → 「$0.20 / $1.20」 → 「$0.10 / $0.50」
  Add a tiny but readable note: 「* GPT-5.6 Solは期間限定」 and 「Terraは現行API掲載中」. Make the downward movement for Sol and Luna visually clear without changing their values.
- Center region, largest focal card: label 「同じ10万入力 + 10万出力」, then large comparison 「GPT-5.6 Luna 約$0.14 → GPT-6 Luna 約$0.06」 with 「合計 約57%減」. Under it, make the key shift explicit: 「トークン単価」 → 「必要な品質で完了する作業全体の費用」. Add a small cost stack with these exact short labels: 「入力・出力（推論含む）」「キャッシュ」「やり直し」「ツール料金」「時間」. Do not imply every task uses the sample token amounts.
- Right region, heading 「いまの使い分け仮説」. Use two role cards: 「計画・難しい作業 → GPT-6.1 Sol xhigh」 and 「普段の実行 → GPT-6 Luna xhigh」. Add a small dotted note: 「Terraの役割をSolが担えるかは未確認」.
- Beneath the role cards, add a compact speed/cost ladder headed 「GPT-6.1 Sol / Standard比」: 「Batch・Flex 0.5x」「Standard 1x」「Fast 2x」「Ultrafast 6x」. The article says Ultrafast is six times Standard. Add the caveat 「入力272Kトークン超はリクエスト全体に長文脈料金」.
- Add a small, clearly qualified benchmark note: 「AutomationBench / GPT-6 Luna high: +5.4ポイント、タスク費用 −58%」 and 「特定ベンチマークの結果」. Do not generalize it to all work.
- Preserve the explicit point that Terra's successor is absent from the GPT-6 main lineup, while GPT-5.6 Terra remains listed as an API model. Do not imply Terra was discontinued.
- Mikuku stands to the right of the chart, with a mildly surprised, thoughtful expression, eyes directed to the central 「約$0.14 → 約$0.06」 comparison. Her bubble says 「単価だけじゃなく、仕事全体の費用で見てみたいです…！」.
- The only displayed prices and benchmark values must be the exact ones listed above. Use no unsupported dates, model names, statistics, or claims. Keep all footnotes legible and do not let decorative art compete with the charts.

## Deviation Record

none

## Negative constraints

No corporate slide deck aesthetic, no flat UI-only design, no photorealism, no strong sci-fi styling, no dark palette, no faint small text, no crowded unreadable footnotes, no new prices or labels, no extra characters, no altered twin-tail hairstyle or hair accessories, no held pen, marker, pointer, notebook, board, or other object. Mikuku remains clearly recognizable at the specified 15–20% presenter scale. Do not let Mikuku hold any objects.
