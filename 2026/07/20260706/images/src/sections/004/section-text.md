# 004. 対応範囲外または限定対応

## 主題

- miku-xlsx2md は Excel の見た目再現 converter ではない
- visual / layout-heavy な要素は対象外または限定対応

## 対応外の例

- .xls / .csv
- exact cell width / row height
- 印刷範囲 / page break
- freeze panes / view state
- font family / font size
- 条件付き書式
- macro / VBA
- OCR

## 限定対応の例

- 罫線: 表検出の手掛かり
- 背景色 / 文字色: 基本は Markdown 色指定にしない
- chart: metadata 抽出
- shape: source-oriented data と一部 SVG

## 対比

| しないこと | すること |
| --- | --- |
| 見た目を全部写す | 読める情報を取り出す |
| Excel を置き換える | Excel を読む入口を作る |

## 吹き出し案

「全部を写すより、読める情報を安定して出すのが大事なのです…」