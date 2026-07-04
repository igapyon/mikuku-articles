# はじめに

- `miku-pptx2md`
- PowerPoint `.pptx` を Markdown へ
- 見た目再現ではなく、AI agent が読みやすい構造化
- Word 文書とは違い、PowerPoint はスライド単位

```text
スライド順
  + 図形テキスト
  + 箇条書き
  + 表
  + ノート
  + 画像参照
  -> Markdown の入口
```

- 地味な対応表と CLI 確認が、後の AI 活用の足場になる

