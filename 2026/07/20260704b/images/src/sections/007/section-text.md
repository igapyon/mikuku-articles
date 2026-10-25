# 基本コマンド

- 変換は入力 Markdown と `--out` が基本

```text
node miku-md2docx-0.9.2.mjs input.md --out output.docx
java -jar miku-md2docx-java-0.9.1.jar input.md --out output.docx
```

- `--out` は必須
- DOCX を標準出力へ出す CLI ではない
- まずは DOCX 主出力だけ

