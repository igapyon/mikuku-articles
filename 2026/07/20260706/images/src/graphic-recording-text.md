# miku-xlsx2md v1.3.0 グラレコ制作用整理テキスト

## 1. これは何？

- Excel workbook `.xlsx` を Markdown へ変換する小さな道具
- 目的は、見た目の完全再現ではなく、AI agent が読みやすい artifact 作り
- Workbook / Sheet / Cell / Table / Formula / Drawing の情報を追跡しやすくする

## 2. 全体の流れ

```text
Excel workbook
  ↓
miku-xlsx2md
  ↓
combined Markdown + assets
  ↓
summary / front matter で確認
  ↓
AI agent が読む
```

## 3. 変換の中心

| Excel 側 | Markdown 側 |
| --- | --- |
| workbook | combined Markdown |
| worksheet | `## Sheet:` |
| 表らしいセル範囲 | pipe table |
| 表外セル群 | paragraph / list |
| 結合セル | merge token |
| 数式セル | cached / evaluated / fallback |
| image / chart / shape | metadata / assets |

## 4. 重要な対比

| 完全再現ではない | 読むための入口 |
| --- | --- |
| cell width / row height は再現しない | sheet 構造を残す |
| 色や罫線描画を写さない | 表検出の手掛かりにする |
| Excel 全関数互換ではない | cached value と fallback を明示 |
| dashboard を絵として再現しない | metadata と summary で確認 |

## 5. runtime の関係

```text
Node.js 版
  └─ 単一 workbook 変換

Java 版
  ├─ 単一 workbook 変換
  └─ directory batch conversion
```

## 6. mode の見方

- output mode: display / raw / both
- table detection mode: balanced / border / planner-aware
- formatting mode: plain / github
- front matter: include / exclude
- shape details: include / exclude

## 7. 数式セルの読み方

```text
cached value
  ↓
AST evaluator
  ↓
legacy resolver
  ↓
式文字列保持
```

- 値が出ても、必ず再計算されたとは限らない
- status と source を見る
- fallback は信頼の置き方を変える合図

## 8. おすすめの使い方

```text
まず --out で Markdown 化
  ↓
--summary で全体像を見る
  ↓
必要なら --zip で asset も出す
  ↓
不明点は元 Excel を見返す
```

## 9. まとめ

- Excel を Markdown に置き換えるのではない
- Excel を読むための地図を作る
- 人と AI agent の両方に届きやすい形へ近づける
