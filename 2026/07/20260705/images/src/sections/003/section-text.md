# 表現対応表

- PowerPoint 側の表現を Markdown 側へ対応づける
- slide order は `ppt/presentation.xml` と relationship から解決
- title placeholder は slide heading
- body text は段落
- ordinary shape text は blockquote
- table は GFM pipe table
- speaker notes は `### Speaker Notes`

```text
PowerPoint 表現
  -> Markdown 表現
  -> AI が読みやすい構造
```

- 図形の見た目ではなく「図形由来テキスト」を残す

