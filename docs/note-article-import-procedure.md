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
```

The common mapping is:

- `images/000.jpg`: cover image, placed immediately after the H1 title.
- `images/001.jpg` and later: section images, placed immediately after the
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
for p in $(rg -o 'images/[0-9]{3}\.jpg' 2026/YYYYMMDD/YYYYMMDD-article-slug.md); do
  test -f "2026/YYYYMMDD/$p" || printf 'missing %s\n' "$p"
done
```

If the article has metadata sections such as `想定読者`, `使用ツール`, or `関連リンク`,
do not add images there unless there is a specific article image for those sections.
In the current article style, images are usually inserted for the main visible
article sections from the cover through `おわりに`.

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
- Confirm the article title appears as an H1 immediately after front matter.

Suggested commit message pattern:

```text
Import YYYYMMDD Note article
```
