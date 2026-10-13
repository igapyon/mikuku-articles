# Image Generation Prompt

## Task

Create one horizontal Japanese graphic-recording explainer poster for the article. Make the flow of daily records easy to understand at a glance. Do not invent features, dates, statistics, or guarantees.

## Style Contract

- style-profile: mikuku-graphic-recording-v1
- horizontal 3:2 technical graphic-recording poster
- uniformly bright white to very pale ivory background (#FFFDF5-like), subtle warm paper tone, soft hand-drawn lines
- dark, high-contrast Japanese labels, including small notes; use pastel colors for borders and arrows rather than faint text
- no dark vignette, muddy brown cast, heavy aged-paper shading, or shadows behind text
- at least left, center, and right regions; make the article-grounded main flow the largest diagram
- show Mikuku clearly as the explaining character, around 15–25% of the canvas, one character only
- include one short speech bubble from the article-specific design
- no scenic background decoration and do not give Mikuku an object to hold
- みくくに物を持たせない

## Article-specific Design

### Main subject and relation

Title: 「日々の予定とタスクを、AIに話しかけて整える」

- layout-family: flow
- primary-relation: 自然な言葉で依頼し、Skillが予定・タスク・活動記録をMarkdownへ整理し、day-planで今日と近い予定を見渡す
- Draw the dominant flow: `いつもの言葉で依頼 → igapyon-miku-daybook Skill → 予定 / タスク / 活動記録のMarkdown → day-plan → 人が確認`
- Label the three record types separately. Include a small note that an existing task is searched before a duplicate is added.

### Regions

- Left: Three exact illustrative requests grounded in the article: add the practice meeting at ○○ Hall on October 15 from 19:00 to 21:00; add the task 「交通費精算」 with planned work day 10/12 and submission deadline 10/16; record 「今日、交通費の明細をまとめた」 as an activity. Do not change the practice meeting into a piano or other activity, do not call the task a business trip, and do not invent dates or receipts.
- Center: The Agent Skill routes each request into the right Markdown record: schedule, task, or activity log. Show task and activity log as separate cards. Show that records remain readable and editable outside the conversation.
- Right: A generated day-plan combines today's planned work, work starting soon, schedules in the coming week, tasks past their planned period, and tasks whose dates need confirmation. A person reviews the list and may update the source records.
- Small lower callouts: `作業予定期間 ≠ 外部締切`; `活動記録 ≠ タスク完了`; weekly activity notes can help prepare a weekly report. Optional `GitHub Actions → GitHub Issue` notice: around 6:00 JST is a standard-setting guide, and scheduled runs may be delayed or missed.
- Small prerequisite note: day-plan generation requires the daybook script, Node.js, and dependency packages.
- In the central Markdown examples, use only the exact schedule, task and activity examples above. The activity example has no explicit calendar date.

### Article phrases to preserve

Use these article-grounded terms in the diagram or nearby design notes. Draw a concise selection so the poster stays readable:

- AIエージェント
- いつもの言葉
- igapyon-miku-daybook
- 予定 / タスク / 活動記録
- Markdown
- 今日の作業
- 近々1週間の予定
- 作業予定期間と締切
- 活動記録とタスク完了
- 会話を閉じても読み返せる
- 週次報告
- GitHub Actions → GitHub Issue
- 午前6時ごろ（目安） / 遅延・未実行あり

### Accuracy constraints

- The Skill is a set of rules for an AI agent to work with a daybook; do not depict it as the Markdown record itself.
- day-plan uses planned work periods. Do not imply that it automatically extracts an external deadline written only in task text.
- An activity log entry does not mark a task complete if remaining work such as submission is unfinished.
- The day-plan is generated from records at that time; regenerating it overwrites the file for the same target date. If space allows, use a compact note: `再生成は同じ日付を上書き`.
- GitHub Actions notification is optional and not guaranteed at an exact time.
- Do not state that plans, deadlines, or tasks are automatically added without the user asking.

### Mikuku and speech bubble

Use the following canonical Mikuku prompt as the identity reference. Keep her face shape, eyes, hair color, long twin-tails and black ribbons with deep-red trim. Preserve the gentle anime technical-explainer impression. She is on the right, looking toward the central flow with a calm, reassuring expression. Do not give Mikuku an object to hold; みくくに物を持たせない。

Speech bubble, exactly or with only a small faithful shortening: 「まずは予定を一つ、言葉で残してみましょう…！」

### Canonical Character Prompt

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

### Character identity rules

- same character
- do not redesign
- preserve character identity
- canonical character prompt
- keep Mikuku's face shape, eye style, hair style, hair color, twin tails, hair accessories, and gentle bright anime technical-explainer impression

## Deviation Record

- none
