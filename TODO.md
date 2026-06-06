# TODO

## Article Images Not Yet Imported

This list tracks articles that still need article-specific cover and section
images. Shared images such as `../images/byMikuku-3.png`,
`../images/useTools-3.png`, and `../images/relatedArticles.png` are not counted as
article-specific images.

The expected pattern is:

- Cover image immediately after the H1 title.
- Section images immediately after the main `##` headings.
- Metadata sections such as `執筆担当`, `想定読者`, `使用ツール`, `関連リンク`,
  `関連記事`, `参考情報`, `参考リンク`, and `実行ページ` do not require dedicated
  article images unless an article-specific image already exists.

For articles whose original local image workspaces are no longer available, use
the recovery/import label `Note掲載済み画像をローカル正本へ再取得`. The images were
uploaded by the owner to the corresponding published Note article, so recover
them from the Note URL in front matter and place them back into the local article
package in cover/section order.

### Note Image Recovery Targets

All articles in this table have a published Note URL in front matter and no local
article-specific cover or main section images yet. They are targets for
`Note掲載済み画像をローカル正本へ再取得`.

| Article | Main sections | Note URL |
| --- | ---: | --- |
| `2026/20260320/20260320-gpt54-app-dev.md` | 11 | https://note.com/toshikiigaa/n/ncc28f9a0fcbd |
| `2026/20260326/20260326-xlsx2md-grid-bug-diary.md` | 7 | https://note.com/toshikiigaa/n/ne63f03142852 |
| `2026/20260327/20260327-xlsx2md-strike-meaning.md` | 7 | https://note.com/toshikiigaa/n/nc0f61d0f1bb2 |
| `2026/20260330/20260330-mikuproject-ai-wbs-draft.md` | 7 | https://note.com/toshikiigaa/n/nf5b9674d2cad |
| `2026/20260330/20260330-mikuproject-intro.md` | 7 | https://note.com/toshikiigaa/n/n20f5ee782358 |
| `2026/20260410/20260410-mikuproject-agent-skills-wbs-planning.md` | 8 | https://note.com/toshikiigaa/n/n87fd2d87bdf5 |
| `2026/20260412/20260412-ai-score-abc-first.md` | 6 | https://note.com/toshikiigaa/n/n5362ea076328 |
| `2026/20260412/20260412-miku-abc-player-intro.md` | 5 | https://note.com/toshikiigaa/n/n5be1d51d336a |
| `2026/20260428/20260428-general.md` | 4 | https://note.com/toshikiigaa/n/nca7cdb17f5db |
| `2026/20260430/20260430-general-ai-dev-docs-todo.md` | 9 | https://note.com/toshikiigaa/n/n5dcb66e47151 |
| `2026/20260509/20260509-agent-skills-activation.md` | 11 | https://note.com/toshikiigaa/n/nfd0dda4c85b4 |
| `2026/20260509/20260509-agent-skills-docs.md` | 7 | https://note.com/toshikiigaa/n/n87a21add286b |
| `2026/20260510/20260510-general-mcp-server-client-local.md` | 11 | https://note.com/toshikiigaa/n/ne87c899f68d2 |
| `2026/20260514/20260514-agent-skills-natural-language-programming.md` | 10 | https://note.com/toshikiigaa/n/ned521551398c |
| `2026/20260515/20260515-general-ai-understand-change-verify-unit.md` | 10 | https://note.com/toshikiigaa/n/n923232b6a9cd |
| `2026/20260516/20260516-content-agent-skills.md` | 13 | https://note.com/toshikiigaa/n/n72da1e228062 |
| `2026/20260516/20260516-general-markdown-gfm-introduction.md` | 27 | https://note.com/toshikiigaa/n/nc9c66635f525 |
| `2026/20260516/20260516-miku-text-bundle-ai-text-assets.md` | 11 | https://note.com/toshikiigaa/n/n5b18c376b2f0 |
| `2026/20260523/20260523-content-agent-skill-types.md` | 16 | https://note.com/toshikiigaa/n/n0ebcb626b082 |
| `2026/20260526/20260526-agent-skills-basic-machine-language.md` | 9 | https://note.com/toshikiigaa/n/n142354986e19 |
| `2026/20260527/20260527-general-ai-agent-does-not-read-all-source.md` | 11 | https://note.com/toshikiigaa/n/n80a82f70fe7c |
| `2026/20260527/20260527-general-openai-codex-surfaces.md` | 16 | https://note.com/toshikiigaa/n/n1234a1d255a9 |
| `2026/20260528/20260528-general-character-persona-technical-essay.md` | 12 | https://note.com/toshikiigaa/n/ne68cf56c07f3 |
| `2026/20260529/20260529-agent-skills-development-assets-germination-growth.md` | 11 | https://note.com/toshikiigaa/n/ne9593f75fccd |
| `2026/20260529/20260529-general-ai-agent-cli-text-json.md` | 12 | https://note.com/toshikiigaa/n/na7fb76c52fda |

### Partially Recovered From Local Workspaces

These articles had some image assets irregularly recovered from
`/Users/igapyon/Documents/git/igapyon-agent-skills/workplace`. This is not the
standard recovery route and should not be assumed for other articles. These
recovered images were not downloaded from the Note site. Remaining missing images
can still be recovered from the published Note article if needed.

| Article | Local recovery status | Remaining work |
| --- | --- | --- |
| `2026/20260428/20260428-miku-indexgen-intro.md` | Cover image `images-miku-indexgen-intro/000.png` imported from `20260531125919-graphic-recording`. | Main section images are still missing. |
| `2026/20260514/20260514-general-ai-engineering-overview.md` | Cover image `images-ai-engineering-overview/000.png` imported from `20260524205052-graphic-recording`. | Main section images are still missing. |
| `2026/20260514/20260514-general-ai-native-cli-mcp-agent-skills.md` | Section images `images-ai-native-cli-mcp-agent-skills/001.png` through `008.png` imported from `20260524210328-section-graphic-recording`. | Cover image and section images `009` through `015` are still missing. |

### Already Has Article Images

These articles already have cover and main section images. Keep them out of the
image-import TODO unless a missing or broken link is found later.

| Article | Main sections |
| --- | ---: |
| `2026/20260530/20260530-general-ai-subscription-pricing-runway.md` | 10 |
| `2026/20260530/20260530-token-consumption-01-basics.md` | 10 |
| `2026/20260531/20260531-token-consumption-02-reduction.md` | 17 |
| `2026/20260531/20260531-token-consumption-03-agent-skills-reduction.md` | 17 |
| `2026/20260601/20260601-general-generative-ai-model-vectors.md` | 17 |
| `2026/20260603/20260603-general-agent-skills-magic-book.md` | 9 |
| `2026/20260604/20260604-general-mermaid-uml-introduction.md` | 17 |
| `2026/20260605/20260605-general-mcp-magic-circle-outline.md` | 11 |
| `2026/20260606/20260606-general-ai-agent-fairies-outline.md` | 11 |
