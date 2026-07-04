# 007. 基本コマンド

## 主題

- 最小コマンドから始める
- 必要に応じて mode や zip を追加する

## 基本形

- Node.js: `node miku-xlsx2md-1.3.0.mjs input.xlsx --out output.md`
- Java: `java -jar miku-xlsx2md-1.3.0.jar input.xlsx --out output.md`
- ZIP: `node ... input.xlsx --zip output.zip`

## 追加確認

- `--output-mode raw`
- `--output-mode both`
- `--table-detection-mode border`
- `--table-detection-mode planner-aware`

## 使い方の流れ

```text
まず --out
  ↓
必要なら summary
  ↓
画像や図形が多ければ zip
  ↓
確認目的に応じて mode 変更
```

## 吹き出し案

「最初は小さく変換して、必要な確認だけ足すのです…」