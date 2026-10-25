# miku-md2docx グラレコ制作用整理テキスト

# 1. これは何？

- Markdown を Word `.docx` へ変換する小さな道具
- Markdown 正本
- Word 提出
- AI agent と人間のレビュー現場をつなぐ出口

```text
Markdown
  -> miku-md2docx
  -> Word document
  -> 人間に渡す
```

# 2. 役割の境界

| できること | しないこと |
| --- | --- |
| 本文構造を Word へ移す | 凝った帳票設計 |
| 見出し、表、リンク、画像 | 厳密なページレイアウト |
| 編集可能な `.docx` 化 | 既存 template 流し込み |
| local-first 変換 | remote image download |

# 3. 2つの runtime

| runtime | version | 特徴 |
| --- | --- | --- |
| Node.js CLI | v0.9.2 | 基準実装、remark 系 parser |
| Java CLI | v0.9.1 | 代表ケース parity、line-oriented parser |

```text
Node.js: remark-parse + gfm + frontmatter
Java   : line-oriented parser helpers
```

# 4. 表現対応の軸

- 段落 -> Normal paragraph
- `#` - `######` -> Heading1 - Heading6
- list -> bullet / ordered list
- pipe table -> Word table
- fenced code -> Code paragraph
- bold / italic / strike / underline -> run style
- link -> hyperlink
- local image -> embedded image
- front matter -> Word body から除外

# 5. 注意が必要なもの

- remote image URL は download しない
- missing image は summary へ
- unresolved internal link も summary へ
- raw HTML は限定対応
- SVG / WebP / GIF は Word 側表示互換に依存
- table alignment は保持しない

# 6. CLI contract

```text
input.md + --out output.docx
```

- `--out` は必須
- DOCX を stdout へ出す CLI ではない
- `--summary` で点検
- `--summary-out` でファイル保存
- `--verbose` で stderr 診断

# 7. 使いどころ

- Markdown 下書きを Word レビューへ
- AI agent と作った仕様メモを Word 共有へ
- Markdown 正本から配布用 `.docx`
- Word 前提の文書管理へ渡す

# 8. Agent / Web 入口

- Agent Skill 経由では出力形式を明示
- `md -> docx` を明確にする
- Web App は browser UI の別 surface
- CLI と Web では version を混同しない

# 9. まとめ

```text
Markdownで考える
  ↓
Markdownを正本にする
  ↓
miku-md2docxでWordへ渡す
  ↓
人間のレビューに載せる
```

- 魔法の Word 帳票生成ではない
- でも、現場の受け渡しには効く
- 小さく、地味で、役割がはっきりした変換器

