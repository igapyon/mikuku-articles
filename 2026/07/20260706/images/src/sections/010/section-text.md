# 010. Java 版の directory extension

## 主題

- Java 版は directory batch conversion を持つ
- 単一ファイル変換とは使い方を分ける

## Java 固有 option

- `--input-directory <dir>`
- `--output-directory <dir>`
- `--recursive`
- `--verbose`

## 流れ

```text
input directory
  ↓ recursive scan
.xlsx files
  ↓
output directory
  ↓
Markdown files
```

## 注意

- directory 変換では `--out` と `--zip` は使えない
- 単一ファイル出力と batch conversion は別の形

## 吹き出し案

「Java 版だけ、フォルダごとの変換ルートがあります…」