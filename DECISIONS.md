---
purpose: ai-agent-decisions
read_when:
  - before_starting_work
  - when_making_decision
  - when_looping_or_repeating_work
update_when:
  - important_decision_is_made
  - option_is_rejected
  - work_is_deferred
---

# Decisions

This file records important decisions for the AI agent.
Read this before making or revisiting decisions, especially when the work seems to loop.

## 2026-06-24: Preserve the existing TODO.md structure

Reason:
`TODO.md` already contains repository-level article and maintenance tasks, plus
an `## AI Agent Current Tasks` section.

Impact:
AI-agent state updates should edit that section in place and avoid rewriting
unrelated project TODO content.

## 2026-06-24: Treat HANDOFF.md as the compact resume source

Reason:
`HANDOFF.md` already exists and is marked with `purpose: ai-agent-handoff`.

Impact:
When pausing or resuming work, update `HANDOFF.md` with the current topic,
status, and next steps instead of turning `TODO.md` into a long work log.

## 2026-06-25: Use the current article as the prompt example

Reason:
The article needs to show the operating feel of `igapyon-agent-state-management`,
not just describe the file convention abstractly.

Impact:
The prompt-example section should use this article's own workflow: publishing a
mostly Mikuku-drafted article on Note, setting that goal first, then resuming
work and updating state from that goal.
