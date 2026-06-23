---
purpose: ai-agent-goal
read_when:
  - before_starting_work
  - before_finishing_work
  - when_scope_is_unclear
update_when:
  - goal_changes
  - done_conditions_change
  - stop_conditions_change
---

# Goal

This file defines what the AI agent is trying to accomplish.
Read this before starting work, before deciding that work is complete, and whenever scope becomes unclear.

## Objective

Keep this repository's AI-agent working state easy to resume while preserving
the existing article-production TODO structure.

## Done

- `TODO.md` has an `## AI Agent Current Tasks` section that reflects the
  current active work.
- `HANDOFF.md` summarizes the latest resume point without stale claims about
  uncommitted work.
- Important state-management decisions are recorded in `DECISIONS.md`.

## Stop

- Stop and ask the user when the requested article, publication target, or
  repository task is ambiguous enough that editing would risk changing the
  wrong content.
- Stop and ask the user before replacing existing human-maintained TODO
  sections or broad project documentation.
- Stop if `TODO.md`'s `Retry Log` records the same underlying failure three
  times.
