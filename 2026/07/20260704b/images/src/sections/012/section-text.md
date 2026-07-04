# 出力

- 主出力は DOCX
- summary は点検用
- verbose は進捗診断

| 出力 | 条件 |
| --- | --- |
| DOCX | `--out` |
| summary stdout | `--summary` |
| summary file | `--summary-out` |
| diagnostics | `--verbose` |

- summary はエラー一覧ではない
- missing image / unresolved link / unsupportedHtml を確認
- 画像とリンクは公開前チェックに効く

