# グラレコ制作用整理テキスト

対象記事: `[miku-md2pptx] MarkdownをPowerPointへ変換する小さな道具 v0.2.2`

## 1. この記事の中心

- Markdown を正本にする
- PowerPoint deck として人間に渡す
- `miku-md2pptx` は小さな出口
- 目的は practical slide structure
- pixel-perfect layout ではない

```text
Markdown 正本
  ↓
miku-md2pptx
  ↓
PowerPoint presentation
  ↓
会議・説明・レビュー
```

## 2. 入口と出口

| 要素 | 役割 |
| --- | --- |
| Markdown `.md` | 考える場所、修正する正本 |
| `miku-md2pptx` | Markdown 構造をスライド構造へ移す変換器 |
| `.pptx` | 人間へ渡す編集可能な資料 |
| PowerPoint | 最後に見た目を整える場所 |

## 3. 変換の基本ルール

- `#` / `##` heading: 新しい slide
- 段落: editable slide text
- list: bullet paragraph
- simple pipe table: native PowerPoint table
- local image: embedded image
- Markdown link: external hyperlink
- speaker notes comment: notesSlide

## 4. 対比で見る

| 観点 | できる | できない・限定 |
| --- | --- | --- |
| 目的 | 構造をPowerPointへ移す | 完成デザイン自動生成 |
| layout | practical slide structure | pixel-perfect layout |
| image | local PNG/JPEG/GIF | remote URL, absolute path |
| list | bullet-style list | ordered numbering の完全保持 |
| round trip | 代表構造の確認 | 完全復元保証 |
| Java parser | companion runtime | full remark-gfm parity ではない |

## 5. runtime の分岐

```text
Node.js v0.2.2
  - artifact: miku-md2pptx-0.2.2.mjs
  - path 解決: CLI artifact の runtime root 基準

Java v0.2.3
  - artifact: miku-md2pptx-java-0.2.3.jar
  - path 解決: current working directory 基準
```

## 6. 必須コマンドの芯

```text
node miku-md2pptx-0.2.2.mjs input.md --out output.pptx
java -jar miku-md2pptx-java-0.2.3.jar input.md --out output.pptx
```

- `--out` は必須
- `--title` で presentation title を上書き
- `--help` / `--version` は metadata command

## 7. 使いどころ

- AI agent と作った Markdown メモをスライド化
- 研修資料の骨子を PowerPoint へ
- 議論のたたき台を deck として共有
- local-first に変換
- `miku-pptx2md` と組み合わせて代表構造を確認

## 8. 注意するところ

- デザイン完成品ではなく土台
- remote image は自動取得しない
- raw HTML は完全変換しない
- Node.js と Java の version を混ぜない
- path 解決基準の違いを説明する
- Java parser は intentionally small

## 9. 全体まとめ

```text
Markdown で考える
  ↓
Markdown を直す
  ↓
Markdown を正本として残す
  ↓
PowerPoint deck として渡す
  ↓
人間が説明・調整する
```

キーワード:

- 小さな出口
- 編集可能な `.pptx`
- 構造を移す
- local tool
- AI agent と人間の作業場所をつなぐ
- version と runtime を分けて説明
