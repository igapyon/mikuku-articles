# セクション005 グラレコ制作用整理テキスト

## 主題

- 同じ `--template` でも内部の意味は違う
- CLI はそろえる
- 実装は Office 形式ごとに自然な単位へ合わせる

## 3つの世界

| tool | 世界 | 自然な単位 |
| --- | --- | --- |
| Word | 文書 | 本文、段落、スタイル、セクション |
| Excel | workbook | sheet、cell、row、column |
| PowerPoint | deck | slide、master、layout、placeholder |

## 図解

```text
利用者: `--template` で指定
  ↓
内部:
  Word       = styles / section
  Excel      = sheet / cell
  PowerPoint = master / layout
```

## メッセージ

- 見た目の入口はそろえる
- 内側では無理をしない
