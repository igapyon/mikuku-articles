# Image Generation Prompt

Create one wide horizontal graphic recording poster for a Japanese technical essay.

## Core Theme

The article explains a small first step for AI agent state management using three Markdown files:

- `GOAL.md`: defines how the work ends and when to stop
- `TODO.md`: keeps the current working position
- `DECISIONS.md`: records decision reasons

The visual should communicate:

- AI agents and humans can lose purpose, current status, and decision context during long work.
- Keeping everything only in chat is fragile.
- Putting state into project-side Markdown makes it readable by Codex, GitHub Copilot agent, Claude Code, and humans.
- This is a small Context Engineering practice, not a heavy process.
- Start small, but not vague.

## Layout

Wide poster, 16:9 aspect ratio. Clean hand-drawn graphic recording style on a warm off-white paper or whiteboard background.

Left side:

- Problem area titled "会話だけだと迷いやすい"
- Small icons: chat bubbles, fading memory, repeated loop arrow, unclear destination
- Short labels:
  - 目的が曖昧
  - 現在地が不明
  - 判断理由が消える
  - 同じ失敗を繰り返す

Center:

- Large triangle diagram with three Markdown file cards:
  - Top: `GOAL.md` / "終わり方・止まり方"
  - Bottom left: `TODO.md` / "現在地・次の一手"
  - Bottom right: `DECISIONS.md` / "判断理由・巻き戻り防止"
- Use arrows between the three cards to show they work together.
- Add small tags around the cards:
  - `Objective`
  - `Done`
  - `Stop`
  - `Tasks`
  - `Blockers`
  - `Retry Log`
  - `理由`
  - `影響`

Lower center:

- A circular workflow:
  - 作業開始
  - 3ファイルを読む
  - 作業する
  - 更新する
  - Done / Stopで確認
  - 次回再開しやすい

Upper right:

- Text block: "Prompt Engineering から Context Engineering へ"
- Visual contrast:
  - "どうお願いするか" -> "迷わない状態をどう保つか"

Right side:

- Mikuku is explaining the poster while looking toward the central triangle.
- Mikuku should not hold any objects.
- Add one speech bubble:
  - "あ、あの…目的・現在地・判断理由を、そっと外に出すのです…"

Bottom:

- Small cross-tool sharing diagram:
  - Codex
  - GitHub Copilot agent
  - Claude Code
  - 人間
  - all pointing to "Markdown共有メモ"
- Closing phrase:
  - "小さく始める。でも曖昧に始めない。"

## Style

Hand-drawn graphic recording illustration, Japanese tech explainer poster, soft line art, clean readable layout, information-rich but not cluttered, warm off-white background, pastel accents, thin marker lines, arrows, boxes, sticky-note shapes, Markdown document icons, folder icons, simple loop arrows.

Use short Japanese labels. The text should look hand-lettered and readable, but avoid tiny dense paragraphs.

## Mikuku Canonical Character Prompt

Use the following as the canonical character prompt for the same character `Mikuku` / `みくく`.

Do not redesign the character. Preserve character identity. Same character. Canonical character reference. Maintain face shape, eyes, hair color, twin-tails, ribbons, shy uneasy personality impression, soft anime technical explainer atmosphere.

Mikuku must not hold any objects. No pen, no pointer, no marker, no notebook, no board in her hands. Keep hands relaxed and simple, partly hidden by sleeves if useful.

Canonical prompt:

masterpiece, best quality, ultra-detailed anime portrait, head-and-shoulders 1girl, shy uneasy expression, slight 3/4 view, looking to her right and slightly upward.

Warm chestnut-brown eyes with gold flecks, soft blush, worried upward-slanted brows, small downturned pout, fair warm skin, delicate V-U shaped chin.

Soft caramel-chestnut very long twin-tails tied high with black ribbons and deep-red trim, silky wavy hair, asymmetrical curtain bangs, long side strands framing cheeks.

Thin clean line art, soft cel shading, watercolor-like shading, subtle rim light, warm minimal background.

## Avoid

- Do not make it a cold corporate slide.
- Do not use a dark sci-fi interface.
- Do not create a generic anime girl; preserve Mikuku identity.
- Do not let Mikuku hold objects.
- Do not overcrowd with long article paragraphs.
- Do not make all text unreadably small.
- Do not use photorealism.
