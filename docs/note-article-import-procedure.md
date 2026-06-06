# Note article import procedure

## Purpose

This document describes how to import an existing Note article Markdown file into
this repository.

The repository stores Mikuku-authored article packages under date-based directories.
Article images may be added later, so the Markdown article can be imported first.

## Target Layout

Use this path pattern:

```text
2026/YYYYMMDD/YYYYMMDD-article-slug.md
```

Example:

```text
2026/20260605/20260605-general-mcp-magic-circle-outline.md
```

The date directory should match the article date or the date encoded in the source
file name.

## Import Steps

1. Confirm the source Markdown path.

   Example source:

   ```text
   /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-note-writer/references/magic-metaphors/20260605-general-mcp-magic-circle-outline.md
   ```

2. Inspect the source file before importing.

   Check at least:

   - Front matter title, tags, author, published target, writer agent, and URL.
   - Whether the front matter follows this repository's article metadata shape.
   - Main headings.
   - Whether image links are already embedded.
   - Whether image files are available now or will be added later.

3. Create the destination date directory.

   Example:

   ```sh
   mkdir -p 2026/20260605
   ```

4. Copy the Markdown file into the destination directory.

   Example:

   ```sh
   cp /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-note-writer/references/magic-metaphors/20260605-general-mcp-magic-circle-outline.md \
     2026/20260605/20260605-general-mcp-magic-circle-outline.md
   ```

5. Verify that the copied file matches the source.

   Example:

   ```sh
   cmp -s /Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-note-writer/references/magic-metaphors/20260605-general-mcp-magic-circle-outline.md \
     2026/20260605/20260605-general-mcp-magic-circle-outline.md
   ```

   A successful `cmp -s` exits with status `0`.

6. Confirm the repository status.

   ```sh
   git status --short
   ```

   The imported directory should appear as untracked until it is staged.

## Front Matter And Opening Title

Normalize imported articles to match the existing article style in this repository.
Use `2026/20260606/20260606-general-ai-agent-fairies-outline.md` as the current
reference shape.

Recommended front matter keys and order:

```yaml
---
title: 記事タイトル
tags: #生成AI #MCP #AIagent #PromptEngineering #mikuku
author: igapyon
published_to: note
writer_agent: みくく
url: https://note.com/toshikiigaa/n/example
release_date: YYYY-MM-DD
---
```

Notes:

- Keep `title`, `tags`, `author`, `published_to`, `writer_agent`, `url`, and
  `release_date`.
- In unquoted front matter values, do not leave a half-width colon followed by a
  space. For example, write `title: miku-grep 開発日誌：AI agent に選ばれる CLI...`,
  not `title: miku-grep 開発日誌: AI agent に選ばれる CLI...`. The `: ` sequence
  inside a YAML value can be parsed as a mapping separator by some tools and may
  break metadata processing. Use a full-width colon `：` in Japanese titles.
- Remove source-only metadata such as `slide: false` unless it is intentionally used
  by this repository.
- Set `release_date` from the article date or the date encoded in the imported file
  name.
- Preserve the Note URL when it is already known.

After front matter, place the article title as an H1 before the cover image:

```md
# 記事タイトル

![記事タイトル](images/000.jpg)

## はじめに
```

This keeps the local Markdown article consistent with the published article package
style.

## Image Handling

Images can be imported after the Markdown file.

When images are not available yet:

- Do not create placeholder image files unless explicitly needed.
- Keep the Markdown article as copied from the source.
- Add image directories later using the same article date directory.

If an old local image workspace is later found, it may be possible to recover
some images from that workspace. Treat this as an irregular recovery path, not
the standard import route. This is not `Note掲載済み画像をローカル正本へ再取得`.
Keep the distinction clear in `TODO.md`: local workspace recovery means the image
files happened to remain in a local project/workplace directory, while Note image
recovery means the local originals were not found and the already-uploaded Note
images are being downloaded back into the article package.

If the original local image files are no longer available but the article was
already published to Note by the repository owner, treat the work as:

```text
Note掲載済み画像をローカル正本へ再取得
```

In this case, use the article's front matter `url` to inspect the published Note
page and recover the already-uploaded article images back into the local article
package. This is a recovery/import step for images that were uploaded by the
owner, not a new external image source. Downloaded images may not be byte-for-byte
identical to the original local generation files because Note may transform or
serve optimized copies, so preserve the recovered image order and record the
source Note URL when doing the import.

Recommended image path pattern:

```text
2026/YYYYMMDD/images/
```

For generated image prompts and section source text, use:

```text
2026/YYYYMMDD/images/src/
2026/YYYYMMDD/images/src/sections/001/
2026/YYYYMMDD/images/src/sections/002/
```

When image files are later provided, inspect them before editing the article:

```sh
find 2026/YYYYMMDD -maxdepth 3 -type f -print | sort
du -sh 2026/YYYYMMDD 2026/YYYYMMDD/images
sips -g pixelWidth -g pixelHeight 2026/YYYYMMDD/images/*.jpg
sips -g pixelWidth -g pixelHeight 2026/YYYYMMDD/images/*.png
```

The common mapping is:

- `images/000.jpg` or `images/000.png`: cover image, placed immediately after the
  H1 title.
- `images/001.jpg` / `images/001.png` and later: section images, placed immediately after the
  corresponding `##` heading.

For example:

```md
# 生成AIの MCP は、妖精さんへお願いする魔法陣に近い

![生成AIの MCP は、妖精さんへお願いする魔法陣に近い](images/000.jpg)

## はじめに

![はじめに](images/001.jpg)
```

After inserting image links, verify that every referenced image exists:

```sh
for p in $(rg -o 'images/[0-9]{3}\.(jpg|png)' 2026/YYYYMMDD/YYYYMMDD-article-slug.md); do
  test -f "2026/YYYYMMDD/$p" || printf 'missing %s\n' "$p"
done
```

If the article has metadata sections such as `想定読者`, `使用ツール`, or `関連リンク`,
do not add images there unless there is a specific article image for those sections.
In the current article style, images are usually inserted for the main visible
article sections from the cover through `おわりに`.

If the article has `## 関連する記事` and no article-specific image is assigned for
that section, use the shared related-articles image:

```md
## 関連する記事

![関連する記事](../images/relatedArticles.png)
```

The shared image is stored at:

```text
2026/images/relatedArticles.png
```

If the article has `## 執筆担当` and no article-specific image is assigned for that
section, use the shared Mikuku author image:

```md
## 執筆担当

![執筆担当](../images/byMikuku-3.png)
```

If the article has `## 使用ツール` and no article-specific image is assigned for
that section, use the shared tools image:

```md
## 使用ツール

![使用ツール](../images/useTools-3.png)
```

The shared images are stored at:

```text
2026/images/byMikuku-3.png
2026/images/useTools-3.png
```

## Extracting Images From Graphic Recording Workplaces

Some generated article-image workspaces contain many operational files that should
not be imported directly. For example:

```text
workplace/YYYYMMDDHHMMSS-graphic-recording/
```

Before copying, inspect candidate files:

```sh
find /path/to/workplace/YYYYMMDDHHMMSS-graphic-recording -maxdepth 5 -type f -print | sort
find /path/to/workplace/YYYYMMDDHHMMSS-graphic-recording -maxdepth 5 -type f \
  \( -name '*.md' -o -name '*.jpg' -o -name '*.jpeg' -o -name '*.png' \) -print | sort
```

Typical files to import:

- `graphic-recording.png`: article cover or representative image.
- `image-prompt.md`: cover-level image-generation prompt.
- `sections/NNN/graphic-recording.png`: section image.
- `sections/NNN/image-prompt.md`: section image-generation prompt.
- `sections/NNN/section-text.md`: section summary and image intent.

Typical files to ignore:

- `.DS_Store`
- `TODO.md`
- `run-state.md`
- `image-generation-report.md`
- `image-inspection-report.md`
- `copy-generated-image.md`
- `article-image-snippets.md`
- `graphic-recording-text.md`
- `sections/NNN/section-source.md`

Use repository-local names after copying. One proven mapping is:

```text
workplace/.../graphic-recording.png              -> 2026/YYYYMMDD/images/000.png
workplace/.../image-prompt.md                    -> 2026/YYYYMMDD/images/src/image-prompt.md
workplace/.../sections/001/graphic-recording.png -> 2026/YYYYMMDD/images/001.png
workplace/.../sections/001/image-prompt.md       -> 2026/YYYYMMDD/images/src/sections/001/image-prompt.md
workplace/.../sections/001/section-text.md       -> 2026/YYYYMMDD/images/src/sections/001/section-text.md
```

Repeat the section mapping for each section directory. Do not copy `section-source.md`
unless there is a specific need to preserve full source excerpts; the current
repository package shape keeps `section-text.md` and `image-prompt.md`.

After copying, insert image links into the article Markdown and refresh `index.json`
with `miku-indexgen`.

## Local System Files

macOS may create `.DS_Store` files inside image directories. These files should not
be committed.

This repository already ignores `.DS_Store`, but it is still useful to remove local
copies before committing:

```sh
find . -name .DS_Store -print
find . -name .DS_Store -delete
```

To confirm that `.DS_Store` is ignored:

```sh
git check-ignore -v 2026/YYYYMMDD/images/.DS_Store
```

To confirm that no `.DS_Store` files are tracked:

```sh
git ls-files '**/.DS_Store' '.DS_Store'
```

## Current Example

The article below was imported using this procedure:

```text
2026/20260605/20260605-general-mcp-magic-circle-outline.md
```

Source:

```text
/Users/igapyon/Documents/git/igapyon-agent-skills/skills/igapyon-note-writer/references/magic-metaphors/20260605-general-mcp-magic-circle-outline.md
```

The Markdown file was copied first. Image files were then added under:

```text
2026/20260605/images/
```

The current image set uses:

- `000.jpg` as the cover image.
- `001.jpg` through `011.jpg` as section images.
- `images/src/image-prompt.md` as the image-generation source prompt.

The article Markdown was then updated to reference those images. The inserted image
links were checked against files on disk.

The imported article was also normalized to this repository's front matter and
opening-title style:

- Removed `slide: false`.
- Added `release_date: 2026-06-05`.
- Added the article title as an H1 immediately after front matter.
- Kept the cover image immediately after that H1.

Another imported image example is:

```text
2026/20260603/images/
```

This package was extracted from a graphic-recording workplace. Only the cover image,
section images, cover `image-prompt.md`, and section `image-prompt.md` /
`section-text.md` files were imported. Operational files such as reports, TODOs,
run state, copy snippets, `.DS_Store`, and `section-source.md` were ignored.

## Commit Checklist

Before committing:

- Confirm only intended files are staged.
- Confirm the copied Markdown file is readable.
- Confirm image files are not accidentally missing if the article already references
  local images that should exist now.
- Confirm `.DS_Store` or other local system files are not included.
- Confirm generated source prompts under `images/src/` are included when they are
  part of the article package.
- Confirm section images are linked in the intended order.
- Confirm front matter follows the repository's standard key set and order.
- Confirm front matter values do not contain unsafe half-width colon-space
  sequences such as `title: ...: ...`; use full-width `：` in Japanese titles.
- Confirm the article title appears as an H1 immediately after front matter.
- Confirm `index.json` is regenerated after adding article Markdown, image prompt
  Markdown, or docs.

Suggested commit message pattern:

```text
Import YYYYMMDD Note article
```
