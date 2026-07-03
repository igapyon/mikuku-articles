# miku-docx2md v1.2.1 グラレコ制作用整理テキスト

# 1. これは何？

- Word `.docx` を Markdown `.md` へ変換する小さな道具
- 目的は「見た目の再現」ではなく「AI agent が読める形」
- 仕様書、手順書、議事録、レビュー資料の入口

```text
Word document
  -> miku-docx2md
  -> Markdown
  -> AI agent
```

# 2. なぜ重要？

- Word は人間には見えるが、AI agent には扱いにくいことがある
- Markdown にすると検索、差分、引用、レビューがしやすい
- 変換範囲を明記すると、AI agent の誤解を減らせる

# 3. 変換されるもの

| Word 側 | Markdown 側 |
| --- | --- |
| 段落、見出し | 段落、`#` 見出し |
| 箇条書き、番号付き | Markdown list |
| 表 | GFM pipe table |
| bold / italic / underline / strike | Markdown / HTML inline |
| link / bookmark | Markdown link / anchor |
| コメント | footnote 風 comment |
| 校閲 | `<ins>` と `~~削除~~` |
| 画像 | placeholder または asset link |

# 4. 対応しないもの

- Word のページレイアウト完全再現
- 色、文字サイズ、フォント、配置
- header / footer / footnote / page number
- SmartArt、WordArt、chart、複雑な drawing layout
- `docx -> md -> docx` の完全復元

```text
できる: 意味を Markdown に寄せる
できない: Word の見た目をそのまま再現
```

# 5. 実行入口

Node.js 版:

```text
node miku-docx2md-1.2.1.mjs input.docx --out output.md
```

Java 版:

```text
java -jar miku-docx2md-1.2.1.jar input.docx --out output.md
```

- `--out`: Markdown 出力
- `--assets-dir`: 画像 asset と manifest
- `--summary-out`: 変換 summary
- `--debug`: 未対応要素 trace
- `--front-matter exclude`: YAML front matter を省略

# 6. Node.js 版と Java 版

| runtime | 得意な形 |
| --- | --- |
| Node.js CLI | 単一 `.docx` 変換 |
| Java CLI | 単一変換 + batch / directory 変換 |

Java 版だけ:

- 複数 input
- `--input-directory`
- `--output-directory`
- `--recursive`

# 7. 出力の考え方

```text
主出力: Markdown
補助: Summary
補助: Asset directory
補助: Asset manifest
診断: Debug trace
```

- 普段は Markdown だけで開始
- 必要になったら summary / assets / debug を追加
- 画像 path は壊れにくい形へ調整
- コメントや校閲は確認材料として残す

# 8. 向いている用途

- Word 仕様書を AI agent に読ませる
- Word 手順書から TODO やレビュー観点を抽出
- 校閲、コメント、メモを確認材料にする
- Git で差分確認しやすい派生物を作る
- Word 正本とは別に AI 作業用 Markdown を作る

# 9. まとめ

- miku-docx2md は「小さな橋」
- Word の中の情報を Markdown へ寄せる
- できること、できないことを明示する
- 人間にも AI agent にも届きやすくする

```text
Word に閉じた情報
  -> Markdown で開く
  -> 人と AI agent が扱いやすくなる
```

