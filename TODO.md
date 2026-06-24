# TODO

## AI Agent Current Tasks

This section tracks active work items for AI agents.
Update this section while working. Do not rewrite unrelated TODO items.

### Tasks

- [ ] Prepare the new 2026-06-25 Note article draft:
  `2026/06/20260625/20260625-general-agent-state-management-skill.md`.
  - Topic: follow-up to the 2026-06-22 AI-agent state-management article,
    focused on making the GOAL/TODO/DECISIONS/HANDOFF workflow into the
    `igapyon-agent-state-management` Agent Skill.
  - Goal, 2026-06-25: publish this Mikuku-drafted article on Note.
  - Current state, 2026-06-25: final wording review is in progress; the user
    wants the article to show the concrete prompt/operator feel of using
    `igapyon-agent-state-management` for this article's own publication flow.
  - Next intended check: refine the prompt-example section around the concrete
    goal "publish this article on Note", then review metadata, related links,
    and whether the article should receive graphic-recording images before
    publication.
  - Observed current workflow for the article text:
    - Create a temporary image-work folder under `Downloads`.
    - Current folder:
      `Downloads/20260625-general-agent-state-management-skill-images`.
    - Copy the article Markdown into that folder:
      `20260625-general-agent-state-management-skill.md`.
    - Graphic-recording execution steps observed so far:
      - Read `igapyon-mikuku-agent` and its `graphic-recording.md` workflow.
      - Read the copied article Markdown from the `Downloads` temporary folder.
      - Create a run directory under the temporary folder's `workplace/`.
      - Create `run-state.md`, `graphic-recording-text.md`, and
        `image-prompt.md`.
      - Run `image_gen` using the generated image prompt.
      - Find the generated PNG under `.codex/generated_images/`.
      - Create `copy-generated-image.md` before copying the PNG into the run
        directory as `graphic-recording.png`.
    - Result: generated PNG was copied to the run directory as
      `graphic-recording.png`, verified as a 1536 x 1024 PNG, and visually
      checked as usable for the article's graphic-recording material.
    - Next step: decide how to bring the generated PNG back into the main
      article package.
    - Use this concrete workflow as source material for the article's
      `## この記事で使うなら` section.
  - GitHub handling:
    - Use GitHub as an intermediate save point while the article is still being
      finalized, when requested.
    - At completion, ensure the fully prepared article content is stored in
      GitHub.
    - Treat commands such as `git add`, `git commit`, and `git pull` as means,
      not as the goal itself.
- [x] Finish pre-publication checks for
  `2026/06/20260624/20260624-general-agent-skills-model-specific-driving-layer.md`.
  - Current state, 2026-06-24: user clarified this file is already after the
    intended Mikuku article checker application.
  - Verification result, 2026-06-24: article footer was completed; local
    image/link references were checked after the footer update.
  - The article remains `status: draft` with `url: ((TBD))`.
- [x] Refresh AI agent state-management files for the current repository state.
  - Current finding, 2026-06-24: before this refresh, `git status --short`
    was clean; after the refresh, only state-management files are changed.
  - Added lightweight `GOAL.md` and `DECISIONS.md`.
  - Updated `HANDOFF.md` so it no longer reports an active uncommitted article
    diff.
- [x] Re-check `igapyon-agent-state-management` after starting a new Codex
  thread or reloading/restarting Codex.
  - Current finding, 2026-06-23: the skill exists at
    `/Users/igapyon/.codex/skills/igapyon-agent-state-management/SKILL.md`,
    with `index.json`, `references/`, and `templates/`.
  - Earlier finding: that conversation's loaded skill list did not include it,
    so it appeared to be a session skill-list snapshot issue rather than a
    missing local file.
  - The same earlier pattern was observed for `igapyon-miku-text-bundle` and
    `igapyon-skill-compactor`: local `SKILL.md` files existed under
    `/Users/igapyon/.codex/skills`, but those skills were not listed in that
    session's available skills.
  - `com.apple.quarantine` is present, but it is also present on skills that
    are visible in the session, so it is probably not the primary cause.
  - Earlier open question: why did Codex omit these local skills from the
    loaded skill list?
  - Earlier re-check result, 2026-06-23: after explicitly naming the skill in a
    new conversation, the skill was still absent from the loaded skill list, but
    the local `SKILL.md` could be read and applied manually.
- [x] If the skills are still missing after a new thread or app restart,
  investigate Codex's local skill discovery path, cache files, and any install
  or enablement step that may be required beyond placing files in
  `/Users/igapyon/.codex/skills`.
  - Investigation result, 2026-06-23: the three locally installed skills that
    are absent from the loaded skill list (`igapyon-agent-state-management`,
    `igapyon-skill-compactor`, and `igapyon-miku-text-bundle`) all contain
    `policy.allow_implicit_invocation: false` in `agents/openai.yaml`.
  - Visible hard-trigger skills such as `igapyon-miku-prompt-lint` and
    `igapyon-ffmpeg-helper` do not use that policy field. The likely cause is
    that Codex excludes skills with `allow_implicit_invocation: false` from the
    session's always-available skill list, even though the local `SKILL.md`
    files exist.
  - Verification result, 2026-06-23: in the current fresh session,
    `igapyon-agent-state-management`, `igapyon-skill-compactor`, and
    `igapyon-miku-text-bundle` are all visible in the available-skills list.
  - Follow-up result, 2026-06-23:
    `/Users/igapyon/Documents/git/miku-text-bundle-skills/TODO.md` was updated
    to mark fresh-session verification complete.

### Blockers

- None currently.

### Retry Log

- No repeated failure yet.

## Current Article Work

- [ ] Continue drafting
  `2026/06/20260619/20260619-agent-skills-rag-step-03-distilled-answer-skeleton.md`.
  - Working topic: Agent Skills RAG step3, distilled Markdown as a context map.
  - Current focus: keep repository roles explicit. This `mikuku-articles`
    repository stores the article draft. The `SKILL.md` and
    `references/distilled/` paths discussed in the article belong to the
    Agent Skill repository used as the article's example target, not necessarily
    to this article repository.

## miku-indexgen Feedback TODO

- [ ] Feed back the distilled Markdown front matter convention from the
  Agent Skills RAG step3 article to `miku-indexgen`.
  - Context: `2026/06/20260618/20260618-agent-skills-rag-step-03-distilled-answer-skeleton.md`
  - Decision from the article design:
    - Use `category: distilled` for every distilled Markdown file.
    - Use `topics` for the finer role, such as `agent-skills`,
      `directory-structure`, `rag`, `token-efficiency`, `reading-order`, and
      `answer-skeleton`.
    - Use `sources` for provenance, meaning the raw corpus or major source
      articles used to create the distilled note.
    - Prefer documented `miku-indexgen` front matter fields instead of custom
      fields such as `doc_type` or `distilled: true`, because undocumented
      fields are intentionally ignored by generated `index.json`.
  - Candidate distilled front matter shape:

    ```yaml
    ---
    title: mikuku-articles における Agent Skills の見方
    description: mikuku-articles の記事群が Agent Skills をどう捉えているかを短くまとめた蒸留 Markdown。
    category: distilled
    topics:
      - distilled
      - agent-skills
      - philosophy
      - answer-skeleton
    status: draft
    audience:
      - agent
      - maintainer
    created: 2026-06-18
    updated: 2026-06-18
    sources:
      - type: local-file
        path: references/raw/mikuku-articles
        role: primary
    ---
    ```

## Skill Example Promotion TODO

- [ ] Copy `2026/06/20260612/20260612-general-ai-conversation-dynamics.md` to an
  `igapyon-mikuku-agent` article example after the article is finalized.
  - Purpose: preserve it as a representative Mikuku-authored technical essay
    about AI conversation dynamics, feedback, common ground, and the soft
    boundary around "heart" without making it a technical claim.
  - Candidate destination:
    `/Users/igapyon/.codex/skills/igapyon-mikuku-agent/examples/articles/`
  - Do this after final publication edits and URL metadata are settled.

## Note Update TODO: Related Articles Section

This list tracks local Markdown changes that still need to be reflected on the
published Note pages.

Change set:

- Rename `## 関連記事` to `## 関連する記事`.
- Keep `## 関連リンク` as a separate section.
- Always include the Note article index link in `## 関連する記事`:
  - `[note記事一覧](https://note.com/toshikiigaa/n/nde411c861a5a)`

Status legend:

- Local: whether the Markdown in this repository has been updated.
- Note: whether the corresponding published Note article has been updated and checked.

| Local | Note | Article | Note URL |
| --- | --- | --- | --- |
| [x] | [ ] | `2026/03/20260320/20260320-gpt54-app-dev.md` | https://note.com/toshikiigaa/n/ncc28f9a0fcbd |
| [x] | [ ] | `2026/03/20260326/20260326-xlsx2md-grid-bug-diary.md` | https://note.com/toshikiigaa/n/ne63f03142852 |
| [x] | [ ] | `2026/03/20260327/20260327-xlsx2md-strike-meaning.md` | https://note.com/toshikiigaa/n/nc0f61d0f1bb2 |
| [x] | [ ] | `2026/03/20260330/20260330-mikuproject-ai-wbs-draft.md` | https://note.com/toshikiigaa/n/nf5b9674d2cad |
| [x] | [ ] | `2026/03/20260330/20260330-mikuproject-intro.md` | https://note.com/toshikiigaa/n/n20f5ee782358 |
| [x] | [ ] | `2026/04/20260410/20260410-mikuproject-agent-skills-wbs-planning.md` | https://note.com/toshikiigaa/n/n87fd2d87bdf5 |
| [x] | [ ] | `2026/04/20260412/20260412-ai-score-abc-first.md` | https://note.com/toshikiigaa/n/n5362ea076328 |
| [x] | [ ] | `2026/04/20260412/20260412-miku-abc-player-intro.md` | https://note.com/toshikiigaa/n/n5be1d51d336a |
| [x] | [ ] | `2026/04/20260428/20260428-general.md` | https://note.com/toshikiigaa/n/nca7cdb17f5db |
| [x] | [ ] | `2026/04/20260428/20260428-miku-indexgen-intro.md` | https://note.com/toshikiigaa/n/n5b0ac55dce0a |
| [x] | [ ] | `2026/04/20260430/20260430-general-ai-dev-docs-todo.md` | https://note.com/toshikiigaa/n/n5dcb66e47151 |
| [x] | [ ] | `2026/05/20260529/20260529-agent-skills-development-assets-germination-growth.md` | https://note.com/toshikiigaa/n/ne9593f75fccd |
| [x] | n/a | `2026/draft/2026XXXX-mikuscore-skills-intro.md` | draft, `url: ((TBD))` |

## Article Image Recovery Status

This list tracks article-specific cover and section image recovery. Shared images
such as `../../images/byMikuku-3.png`,
`../../images/useTools-3.png`, and `../../images/relatedArticles.png` are not counted as
article-specific images.

The expected pattern is:

- `000`: cover/head image immediately after the H1 title.
- `001` and later: section images immediately after the main body `##` headings.
- Metadata sections such as `執筆担当`, `想定読者`, `使用ツール`, `関連リンク`,
  `関連記事`, `参考情報`, `参考リンク`, and `実行ページ` do not require dedicated
  article images unless an article-specific image already exists.
- For `執筆担当` and `使用ツール`, use the usual shared images unless a special
  article-specific image is clearly specified.

For articles whose original local image workspaces are no longer available, use
the recovery/import label `Note掲載済み画像をローカル正本へ再取得`. The images were
uploaded by the owner to the corresponding published Note article, so recover
only the `000` cover/head image and main body section images from the Note URL in
front matter, then place them back into the local article package in order.

### Note Image Recovery Result

Published Note pages may expose the cover image in
`production/uploads/images/...`, while body images may be exposed separately as
`assets.st-note.com/img/...` entries in rendered figures or structured page data.
The recovery pass now uses both patterns. Some older articles still appear to
have only a cover image, or fewer body images than the local `##` section count.

### Still Missing Some Main Section Images

The articles below have their cover image, but still do not have an image assigned
for every main body `##` section.

| Article | Cover | Sections with image | Missing main sections | Note URL |
| --- | --- | ---: | --- | --- |
| `2026/03/20260320/20260320-gpt54-app-dev.md` | yes | 0/11 | はじめに / 「`xlsx` から `markdown` が欲しい」と思った / 軽い気持ちで始めた実験だった / コードは書かず、たまに観察して育てるシミュレーションゲームのような感覚 / 生成AI は思っていたよりも広く仕事をしてくれた / それでも人間の仕事もあるよ / 生成AI と作ると、コードへの執着がかなり薄くなる / 放置系シミュレーションゲームみたいだね / 画面をあまり使わないアプリだったので人間介入が少なくて済んだんだよね / 今後のソフトウェア開発って、変わっていくのかも。あるいはすでに変わっているのかもね / まとめ | https://note.com/toshikiigaa/n/ncc28f9a0fcbd |
| `2026/03/20260326/20260326-xlsx2md-grid-bug-diary.md` | yes | 3/7 | はじめに / およよ、となった / その場で直してまた進んだ / 記事を書くことも開発の続きなんだなと思った | https://note.com/toshikiigaa/n/ne63f03142852 |
| `2026/03/20260327/20260327-xlsx2md-strike-meaning.md` | yes | 2/7 | 最初は、ただ Excel を Markdown にしたかった / でも、取り消し線は落とせないと思った / 設計書では、取り消し線は状態そのもの / とはいえ、Excel の装飾を何でも Markdown にできるわけではない / まとめ | https://note.com/toshikiigaa/n/nc0f61d0f1bb2 |
| `2026/03/20260330/20260330-mikuproject-ai-wbs-draft.md` | yes | 3/7 | はじめに / 返ってきたものを見て、少し驚いた / 嬉しいけれど、少し怖い感じもあった / まとめ | https://note.com/toshikiigaa/n/nf5b9674d2cad |
| `2026/03/20260330/20260330-mikuproject-intro.md` | yes | 5/7 | はじめに / まとめ | https://note.com/toshikiigaa/n/n20f5ee782358 |
| `2026/04/20260410/20260410-mikuproject-agent-skills-wbs-planning.md` | yes | 5/8 | WBS 作成は、やっぱり面倒 / 実は `Agent Skills` を使ってました / ただし、責任を取るのは人間 | https://note.com/toshikiigaa/n/n87fd2d87bdf5 |
| `2026/04/20260412/20260412-ai-score-abc-first.md` | yes | 2/6 | はじめに / きっかけや背景 / やってみたこと / 起きたこと / 実行ページなど | https://note.com/toshikiigaa/n/n5362ea076328 |
| `2026/04/20260412/20260412-miku-abc-player-intro.md` | yes | 2/5 | はじめに / きっかけや背景 / やってみたこと / 起きたこと | https://note.com/toshikiigaa/n/n5be1d51d336a |
| `2026/04/20260428/20260428-general.md` | yes | 1/4 | はじめに / 「ワイルドカード」が、だんだん減っていく / 会話というより、依頼の練習 | https://note.com/toshikiigaa/n/nca7cdb17f5db |
| `2026/04/20260428/20260428-miku-indexgen-intro.md` | yes | 1/6 | はじめに / きっかけや背景 / やってみたこと / 起きたこと / そこから感じたこと / 実行方法 | https://note.com/toshikiigaa/n/n5b0ac55dce0a |
| `2026/04/20260430/20260430-general-ai-dev-docs-todo.md` | yes | 8/9 | TODO.md は会話を引き継ぐ場所になる | https://note.com/toshikiigaa/n/n5dcb66e47151 |
| `2026/05/20260509/20260509-agent-skills-activation.md` | yes | 6/11 | Agent Skills は、事前に一覧として渡される / description が発火精度を左右する / 作業系 skill の継続 / 会話スタイル系 skill の継続 / 継続中でも優先されるもの | https://note.com/toshikiigaa/n/nfd0dda4c85b4 |
| `2026/05/20260509/20260509-agent-skills-docs.md` | yes | 5/7 | Agent Skills の説明ページは、少し書きづらい / では、人間向けには何を説明するのか | https://note.com/toshikiigaa/n/n87a21add286b |
| `2026/05/20260510/20260510-general-mcp-server-client-local.md` | yes | 9/12 | MCP は AI そのものではない / まず覚えるなら、このくらいでよい / 参考 | https://note.com/toshikiigaa/n/ne87c899f68d2 |
| `2026/05/20260515/20260515-general-ai-understand-change-verify-unit.md` | yes | 9/10 | おわりに | https://note.com/toshikiigaa/n/n923232b6a9cd |
| `2026/05/20260516/20260516-content-agent-skills.md` | yes | 11/13 | `templates/` と `examples/` が出力を安定させる / `CHANGELOG.md` をどうするか | https://note.com/toshikiigaa/n/n72da1e228062 |
| `2026/05/20260516/20260516-general-markdown-gfm-introduction.md` | yes | 18/22 | 章の見出し / 引用 / 区切り線 / 取り消し線 | https://note.com/toshikiigaa/n/nc9c66635f525 |
| `2026/05/20260516/20260516-miku-text-bundle-ai-text-assets.md` | yes | 10/11 | 制限回避ではなく、整理と選択のための道具 | https://note.com/toshikiigaa/n/n5b18c376b2f0 |
| `2026/05/20260523/20260523-content-agent-skill-types.md` | yes | 13/16 | レビュー基準型 / 索引・入口型 / 分類するときに気をつけたいこと | https://note.com/toshikiigaa/n/n0ebcb626b082 |
| `2026/05/20260527/20260527-general-openai-codex-surfaces.md` | yes | 15/16 | 表にすると、少し見えやすい | https://note.com/toshikiigaa/n/n1234a1d255a9 |
| `2026/05/20260528/20260528-general-character-persona-technical-essay.md` | yes | 11/12 | 編集者としての人間、著者としてのみくく | https://note.com/toshikiigaa/n/ne68cf56c07f3 |
| `2026/05/20260529/20260529-agent-skills-development-assets-germination-growth.md` | yes | 10/11 | おわりに | https://note.com/toshikiigaa/n/ne9593f75fccd |
| `2026/05/20260529/20260529-general-ai-agent-cli-text-json.md` | yes | 11/12 | おわりに | https://note.com/toshikiigaa/n/na7fb76c52fda |

### Partially Recovered From Local Workspaces

These articles had some image assets irregularly recovered from
`/Users/igapyon/Documents/git/igapyon-agent-skills/workplace`. This is not the
standard recovery route and should not be assumed for other articles. These
recovered images were not downloaded from the Note site.

| Article | Local recovery status | Remaining work |
| --- | --- | --- |
| `2026/04/20260428/20260428-miku-indexgen-intro.md` | Cover image `images-miku-indexgen-intro/000.png` imported from `20260531125919-graphic-recording`. | Later Note recovery added `005.png` for `まとめ`; main section coverage is still partial. |
| `2026/05/20260514/20260514-general-ai-engineering-overview.md` | Cover image `images-ai-engineering-overview/000.png` imported from `20260524205052-graphic-recording`. | Later Note recovery filled the remaining main body section images. |
| `2026/05/20260514/20260514-general-ai-native-cli-mcp-agent-skills.md` | Cover image `000.png` recovered from Note; section images `001.png` through `008.png` imported from `20260524210328-section-graphic-recording`. | Later Note recovery filled section images `009` through `015`. |

### Already Has Article Images

These articles already have cover and main section images. Keep them out of the
image-import TODO unless a missing or broken link is found later.

| Article | Main sections |
| --- | ---: |
| `2026/05/20260530/20260530-general-ai-subscription-pricing-runway.md` | 10 |
| `2026/05/20260530/20260530-token-consumption-01-basics.md` | 10 |
| `2026/05/20260531/20260531-token-consumption-02-reduction.md` | 17 |
| `2026/05/20260531/20260531-token-consumption-03-agent-skills-reduction.md` | 17 |
| `2026/06/20260601/20260601-general-generative-ai-model-vectors.md` | 17 |
| `2026/06/20260603/20260603-general-agent-skills-magic-book.md` | 9 |
| `2026/06/20260604/20260604-general-mermaid-uml-introduction.md` | 17 |
| `2026/06/20260605/20260605-general-mcp-magic-circle-outline.md` | 11 |
| `2026/06/20260606/20260606-general-ai-agent-fairies-outline.md` | 11 |
