# 何をする Agent Skills なのか

## 主題

- MS Office と Markdown をつなぐ
- converter を agent が迷わず呼ぶための手順と runtime
- 大きなアプリではなく作業の足場

## 図解

```text
ユーザー依頼
  ↓
igapyon-miku-ms-office
  ↓
入力形式を判断
  ↓
miku-soft converter
  ↓
Markdown 出力
```

## 対象

- .docx -> .md
- .xlsx -> .md
- .pptx -> .md

## 短いラベル

- Agent Skills package
- converter 選択
- 手順と runtime
- 人間がコマンドを覚えない
- 小さな足場
