# `--help` 出力の確認

- 生の help は CLI contract の正本に近い
- 入力、必須オプション、summary、diagnostics、exit code をまとめて確認できる

```text
<input.md> --out <output.docx>
--summary
--summary-out <file>
--verbose
--help
--version
```

- missing image と unresolved internal link は summary へ
- 変換は止めない
- 引数不足は exit code 2

