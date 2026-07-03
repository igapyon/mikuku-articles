# 表現対応表

- Word 側の表現が Markdown 側でどう出るか
- 段落、見出し、list、表、inline formatting
- link、bookmark、コメント、校閲、画像
- debug 時は unsupported trace も出せる

## 図解

```text
Word 表現
  -> 変換ルール
  -> Markdown 表現
```

## 代表ラベル

- 見出し -> `#`
- 表 -> pipe table
- コメント -> footnote 風
- 校閲 -> `<ins>` / `~~`
- 画像 -> placeholder / asset link

