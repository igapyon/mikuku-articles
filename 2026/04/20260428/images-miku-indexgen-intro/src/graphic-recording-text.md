# miku-indexgen グラレコ制作用整理テキスト

# 1. 大テーマ

AI エージェントにファイル群を読ませる前に、まず「読む前の地図」を渡す。

```text
ディレクトリ
  ↓
miku-indexgen
  ↓
index.json
  ↓
AI agent が読む候補を選ぶ
```

# 2. なぜ重要？

いきなり全ファイルを読むと重い。

- 関係ないファイルまで読む
- トークン消費が増える
- どこから見ればよいか迷う
- まず全体像だけ知りたい場面が多い

そこで `index.json` を先に見る。

```text
全部読む
  ↓
重い・迷う

先に索引を見る
  ↓
軽い・選べる
```

# 3. miku-indexgen とは？

指定したディレクトリを走査して、ファイル一覧の索引を作る CLI。

主な出力:

| 出力 | 役割 |
|---|---|
| index.json | AI agent / script 向けの正本 |
| index.md | 人間が眺める補助一覧 |

目的は全文検索ではなく、読む前の入口整理。

# 4. index.json に入るもの

AI agent が判断しやすい軽いメタデータを並べる。

- name
- path
- ext
- dir
- size
- summary

構造はフラットな `files` 配列。

```text
files[]
  ├─ README.md
  ├─ docs/usage.md
  └─ config/sample.json
```

階層を深くたどるより、一覧として選びやすくする。

# 5. summary の役割

Markdown なら見出しや本文から概要を拾う。
JSON なら JSON Pointer で `/title` や `/name` を summary 候補にできる。

```text
Markdown heading
JSON title/name
  ↓
summary
  ↓
読む候補の判断材料
```

# 6. どんな場面で使う？

- AI エージェントに読む候補を渡す前処理
- docs 配下の棚卸し
- 記事やメモの一覧生成
- JSON メタデータ付きファイルの整理
- Agent Skills やローカル知識ベースの入口作り

# 7. 設計上の割り切り

小さく、扱いやすくする。

| しないこと | すること |
|---|---|
| 全文検索エンジン | ファイル索引 |
| 高度な意味解析 | 簡易 summary |
| 大きな管理システム | 小さな CLI |
| 全部を読む | まず候補を選ぶ |

# 8. Node.js / Java / Maven

使う場所に合わせて選べる。

- Node.js 版: `npx miku-indexgen`
- Java CLI 版: `miku-indexgen-java`
- Maven plugin: `miku-indexgen-java-maven`

# 9. まとめ

```text
読む前に地図を作る
  ↓
候補を選ぶ
  ↓
必要なファイルだけ読む
  ↓
AI agent の作業入口が軽くなる
```

キーワード:

- 読む前の地図
- index.json
- index.md
- フラットな files 配列
- summary
- トークン消費を抑える
- Agent Skills の入口作り
