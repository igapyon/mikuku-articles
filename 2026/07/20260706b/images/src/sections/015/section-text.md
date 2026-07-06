# セクション整理: Agent Skill 経由で使う

## 主題

- Agent Skill 経由では Markdown から Excel へ出すことを明示する
- Markdown-to-Office 方向では出力形式の明示が重要

## 例

- `convert ./docs/table.md to ./workplace/table.xlsx`
- `use Java backend`
- `.docx`
- `.xlsx`
- `.pptx`

## 注意

- 入力 Markdown だけでは変換先を判断できない
- Word / Excel / PowerPoint の取り違えを避ける
- backend を指定したい場合は Node.js / Java を明示

## 吹き出し案

Markdown を、どの Office 形式へ出すのかを言ってください…！
