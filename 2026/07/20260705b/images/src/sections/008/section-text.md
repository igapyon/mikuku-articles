# `--help` 出力の確認

- CLI 契約を生の help で確認
- 入力、必須 option、title override、Markdown handling notes がまとまる

help で見る要点:

- Usage:
  - `<input.md> --out <output.pptx>`
  - `--help`
  - `--version`
- Options:
  - `--out <path>`
  - `--title <text>`
- Markdown handling notes:
  - Heading level 1 and 2 blocks start new slides
  - paragraphs, lists, code blocks, tables become simple editable slide text
  - structure and local generation over pixel-perfect layout

グラレコ軸:

```text
help output
  ↓
CLI contract
  ↓
AI agent の思い込み防止
```
