---
purpose: ai-agent-handoff
updated: 2026-06-24
---

# HANDOFF

This file summarizes the current AI agent work state for resuming later.

## Current Topic

Pre-publication review of
`2026/06/20260624/20260624-general-agent-skills-model-specific-driving-layer.md`.

The current focus is to keep the article technically correct while preserving
the Mikuku-authored technical essay tone.

There is an active uncommitted diff in the article. The prior commit was:

- `16f57f7 Refine technical caveats in Qwen skills article`

The current uncommitted article edits soften wording around:

- title/description: from "optimal/different" to "looks different"
- Qwen3 framing: from stronger judgment to personal observation
- summary: from "stable" to "looks like it may be stable"

The user then asked for a "みくくチェッカー". The next correct workflow is
likely `igapyon-mikuku-agent` with its text-characteristics/self-review
reference, not just ordinary article-writing tone guidance.

## Earlier Topic

Codex skill discovery issue for locally installed Agent Skills under
`/Users/igapyon/.codex/skills`.

The original symptom was that some local skills existed on disk but did not
appear in the session's available-skills list.

## Findings

Three missing skills were identified:

- `igapyon-agent-state-management`
- `igapyon-skill-compactor`
- `igapyon-miku-text-bundle`

Likely cause found:

- Those missing skills had `policy.allow_implicit_invocation: false` in
  `agents/openai.yaml`.
- Visible hard-trigger skills relied on trigger wording in `SKILL.md` and did
  not use that policy field.

One separate false-positive skill was also identified:

- `__SKILL_NAME__`

Likely cause:

- A template skill lived under a nested path matching a real skill layout:
  `skills/igapyon-miku-soft-developer/assets/agent-skills/skills/__SKILL_NAME__/SKILL.md`.

## Source Repositories

Relevant source repositories:

- `/Users/igapyon/Documents/git/igapyon-agent-skills`
  - owns `igapyon-agent-state-management`
  - owns `igapyon-skill-compactor`
  - owns the `__SKILL_NAME__` template under `igapyon-miku-soft-developer`
- `/Users/igapyon/Documents/git/miku-text-bundle-skills`
  - owns `igapyon-miku-text-bundle`

## Current Status

Observed source TODO state at handoff time:

- `igapyon-agent-skills/TODO.md` says the visibility issue is fixed:
  - `policy.allow_implicit_invocation: false` was removed from the affected
    source `agents/openai.yaml` files.
  - installed copies were updated under `/Users/igapyon/.codex/skills`.
  - a fresh session verified `igapyon-agent-state-management` and
    `igapyon-skill-compactor` appear.
  - the template skeleton was moved out of the nested real-skill shape and
    renamed so `__SKILL_NAME__` no longer appears.
- `miku-text-bundle-skills/TODO.md` says the skill has been updated to
  `v1.3.0`, the local skill has been reinstalled or rebuilt, and
  fresh-session verification is now complete.

Fresh-session verification result, 2026-06-23:

- `igapyon-agent-state-management`, `igapyon-skill-compactor`, and
  `igapyon-miku-text-bundle` all appear in the current session's available
  skills list.
- `/Users/igapyon/Documents/git/miku-text-bundle-skills/TODO.md` was updated to
  mark the fresh-session verification complete.

## Next Resume Steps

1. Continue with the Mikuku checker request by reading
   `/Users/igapyon/.codex/skills/igapyon-mikuku-agent/references/text-characteristics-classification.md`.
2. Review the current article against that checklist.
3. Make only scoped wording changes if the checker finds issues.
4. Commit the article changes if the user asks.
5. No further local skill-discovery investigation is currently needed unless a
   later session regresses.
6. For `miku-text-bundle-skills`, only the explicit release follow-ups remain:
   push tag, create GitHub Release, and upload release assets if requested.

## Local Working Trees At Handoff

At handoff time:

- current repository `/Users/igapyon/Documents/git/mikuku-articles` has a
  modified article plus these state-file updates.
- `igapyon-agent-skills` appeared clean by `git status --short`.
- `miku-text-bundle-skills` appeared clean by `git status --short`.
