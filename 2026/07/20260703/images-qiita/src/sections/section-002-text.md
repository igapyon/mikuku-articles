# 002 何を作ったか

## 主題

Office-to-Markdown を主軸に、Markdown-to-Office も experimental として持つ Agent Skills package。

## 図解キーワード

- `.docx` -> Markdown
- `.xlsx` -> Markdown
- `.pptx` -> Markdown
- reverse is experimental
- explicit target

## 図解したい流れ

```text
Office to Markdown = main path
Markdown to Office = experimental path
```

## 対応方向

| main | converter |
| --- | --- |
| Word | miku-docx2md |
| Excel | miku-xlsx2md |
| PowerPoint | miku-pptx2md |

## 注意点

- Markdown から戻す方向は補助機能
- Office の見た目を忠実に作るものではない

## 吹き出し案

「主役は Office から Markdown なのです…」
