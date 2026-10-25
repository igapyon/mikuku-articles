# 002. 概要

## 主題

- miku-xlsx2md は .xlsx を Markdown と関連 asset に変換する
- AI agent が読むための Markdown-oriented artifact を作る

## 基本の流れ

```text
Excel workbook
  -> miku-xlsx2md
  -> Markdown
  -> AI agent が読む
```

## 扱う情報

- Workbook / Sheet の構造
- Cell / Table の内容
- Formula の表示値や fallback
- Drawing 由来の画像、グラフ、図形 metadata
- YAML front matter

## 重要ポイント

- ピクセル単位の再現ではない
- workbook 単位の combined Markdown
- 既定では YAML front matter から始まる
- `# Book:` と `## Sheet:` で構造を残す

## 吹き出し案

「Workbook の地図を Markdown で作る感じ…かな、って」