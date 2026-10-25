# Agent Skill 経由で使う

- `igapyon-miku-ms-office` 経由で使う場合
- Markdown から PowerPoint へ出すことを明示
- backend を Node.js / Java で指定可能
- Markdown-to-Office では出力形式を明示

例:

```text
igapyon-miku-ms-office: convert ./docs/brief.md to ./workplace/brief.pptx

igapyon-miku-ms-office: use Java backend to convert ...
```

注意:

- Markdown 入力だけでは Word / Excel / PowerPoint の判断ができない
- `.docx` / `.xlsx` / `.pptx` の取り違えを避ける
- 変換先を明示する
