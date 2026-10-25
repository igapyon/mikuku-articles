# 009. 共通オプション

## 主題

- 通常変換は最小構成
- 調査用 option は必要時に opt-in

## option の役割グループ

- 出力先: `--out`, `--zip`
- 文字: `--encoding`, `--bom`
- 値の見方: `--output-mode`
- Markdown 表現: `--formatting-mode`
- 表検出: `--table-detection-mode`
- 図形: `--shape-details`
- front matter: `--front-matter`
- 調査: `--summary`, `--version`, `--help`

## 推奨

```text
input.xlsx --out output.md
  ↓
必要になったら summary / zip / raw / both / shape-details
```

## 吹き出し案

「出力を散らかさないために、確認材料はあとから足します…」