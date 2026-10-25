# セクション整理: 対応 runtime

## 主題

- Node.js 版 v0.6.6 と Java 版 v0.6.5
- 通常利用する CLI 引数はほぼ同じ

## 対比

| Runtime | 特徴 |
| --- | --- |
| Node.js | `remark-parse` + `remark-gfm` AST |
| Java | straight-conversion runtime |

## 共通

- `<input.md>`
- `--out <output.xlsx>`
- `--sheet-mode`
- `--sheet-heading-depth`
- `--title`
- `--table-style`
- `--no-header-row`

## 注意

- version と parser 方針を混同しない
- Java は byte-level parity ではなく semantic workbook output

## 吹き出し案

同じように使えても、中の parser 方針は少し違うのです…！
