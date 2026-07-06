# グラレコ制作用整理テキスト

対象記事: `[miku-md2xlsx] MarkdownをExcelへ変換する小さな道具 v0.6.6`

## 1. この記事の大テーマ

- Markdown を Excel workbook に戻す小さな出口
- Markdown 正本を保つ
- 人間へ渡せる `.xlsx` を作る
- AI agent と人間の作業場所をつなぐ

```text
Markdown
  ↓
miku-md2xlsx
  ↓
Excel workbook
  ↓
人間が確認・共有・編集
```

## 2. 入口と出口

| 要素 | 役割 |
| --- | --- |
| Markdown | 表、メモ、仕様、調査結果の正本 |
| miku-md2xlsx | Markdown 構造を workbook 構造へ移す変換器 |
| Excel workbook | 人間が扱いやすい共有・確認・編集の出口 |

キーワード:

- 入口: Markdown
- 変換: 見出し、段落、表、リンク、画像参照、merge marker
- 出口: 編集可能な Excel workbook

## 3. 変換されるもの

- 見出し: row、または worksheet 分割の境界
- 段落: worksheet row
- list: list row、nested list は列をずらす
- Markdown table: 複数 row / cell
- code block: code row
- link: 単一 link は Excel hyperlink
- local image: best-effort embed
- `[←M←]` / `[↑M↑]`: Excel merge range

図解しやすい並び:

```text
Markdown 表現
  ↓
workbook model
  ↓
worksheet / row / cell / hyperlink / merge / media
```

## 4. できること / しないこと

できること:

- Markdown table や仕様表を Excel 化
- AI agent が作った調査表を Excel として共有
- `miku-xlsx2md` 由来 Markdown を実用 workbook に戻す
- text-oriented な確認表を Excel に渡す
- local-first に workbook を生成

しないこと:

- pixel-perfect な完成帳票
- 元 workbook の完全復元
- native formula / chart / shape / SmartArt の再構築
- remote image URL の自動取得
- 完全 round-trip 保証

## 5. Runtime と CLI

Node.js 版:

- `miku-md2xlsx` v0.6.6
- artifact: `miku-md2xlsx-0.6.6.mjs`
- parser: `remark-parse` + `remark-gfm`
- product core

Java 版:

- `miku-md2xlsx-java` v0.6.5
- artifact: `miku-md2xlsx-java-0.6.5.jar`
- Java straight-conversion runtime
- representative semantic workbook output

共通の最小形:

```text
input.md + --out output.xlsx
```

重要:

- `--out` は必須
- XLSX bytes を stdout に流す前提にしない
- summary JSON などの未確認 option を作らない

## 6. Sheet mode

| mode | 役割 |
| --- | --- |
| `single` | Markdown 全体を 1 worksheet |
| `heading` depth 1 | `#` heading ごとに worksheet 分割 |
| `heading` depth 2 | `##` heading ごとに worksheet 分割 |

`miku-xlsx2md` 風 Markdown では:

```text
# workbook title
## worksheet name
```

として扱いやすい。

## 7. まとめ

- Markdown で考える
- Markdown で直す
- Markdown を正本として残す
- 最後に Excel workbook として渡す

短いメッセージ:

> Markdown の構造を、Excel の編集可能な土台へそっと戻す道具。
