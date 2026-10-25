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

Prepare the 2026-06-25 article for publication on Note:
`2026/06/20260625/20260625-general-agent-state-management-skill.md`.

The article was mostly drafted by Mikuku. The current goal is to complete the
publication workflow: finish the article, publish it on Note, and write the
published Note URL back into the article Markdown.

## Done

- The article reads naturally as a Mikuku-authored technical essay.
- The section about using Agent Skills includes concrete prompts based on this
  article's own publication workflow.
- Graphic-recording PNG files have been created in the relevant
  `Download/<target-directory>` work area and brought back into the main article
  package when needed.
- The article footer is complete, including author, target readers, tools,
  related articles, and related links as appropriate.
- The completed article content is stored in GitHub.
- The article has been uploaded to Note.
- The published Note URL has been recorded in the article Markdown `url` field.

## Stop

- Stop and ask the user when the requested article, publication target, or
  repository task is ambiguous enough that editing would risk changing the
  wrong content.
- Stop and ask the user when the next procedure is unclear, especially for
  publication, GitHub storage, Note upload, or moving generated assets back into
  the main article package. Do not keep proceeding by guessing.
- Stop and ask the user before replacing existing human-maintained TODO
  sections or broad project documentation.
- Stop if `TODO.md`'s `Retry Log` records the same underlying failure three
  times.
