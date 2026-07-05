# 概要

- `miku-md2pptx` は miku-soft 系の小さな変換ツール
- Markdown `.md` を PowerPoint presentation `.pptx` に変換
- 用途: 説明資料、設計メモ、議論のたたき台、研修資料
- 中心は見た目ではなく文書構造

```text
Markdown
  -> miku-md2pptx
  -> PowerPoint presentation
  -> 人間に渡す
```

対比:

| 目指す | 目指さない |
| --- | --- |
| practical slide structure | pixel-perfect PowerPoint layout |
| 編集可能な土台 | 完成済みデザイン |
| Markdown構造の移送 | 細部までの装飾 |
