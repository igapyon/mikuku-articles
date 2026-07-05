# 出力

- 主出力は `.pptx`
- 成功時は stdout に `Wrote ...`
- diagnostics は stderr warnings
- version/help は metadata output

出力分類:

| 出力 | 内容 |
| --- | --- |
| PPTX | 主出力 |
| stderr warnings | skipped image / HTML-like text |
| stdout success | `Wrote ...` |
| stdout metadata | version / help |

画像とリンク:

- local image は入力 Markdown からの相対 path
- remote image URL は skipped
- absolute image path は skipped
- Markdown link は hyperlink relationship
- speaker notes は notesSlide

注意:

- CLI input path 解決と Markdown内 image path 解決を分ける
