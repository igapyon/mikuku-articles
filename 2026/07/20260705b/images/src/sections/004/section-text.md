# 対応範囲外または限定対応

- `miku-md2pptx` は構造変換ツール
- PowerPoint の視覚完成度やテンプレート設計は対象外

対比:

| 対応 | 対象外・限定 |
| --- | --- |
| heading level 1/2 | detailed theme |
| simple pipe table | complex table layout |
| local PNG/JPEG/GIF | remote image URL |
| speaker notes comment | raw HTML full conversion |
| editable deck の土台 | pixel-perfect layout |

図解:

```text
Markdown 構造
  ↓ 変換できる
PPTX の土台
  ↓ 人間が調整
見た目の完成
```

メッセージ:

- 「完成したデザインを一気に作る道具」ではない
- 「説明の骨組みを PowerPoint に起こす最初の一歩」
