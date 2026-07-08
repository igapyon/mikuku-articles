# セクション007 グラレコ制作用整理テキスト

## 主題

- `miku-md2xlsx` のテンプレート適用
- template workbook / sheet を土台にする
- Markdown から生成した値を書き込む

## 図解

```text
template.xlsx
  ├─ sheet 1 の見た目
  ├─ sheet 2 の見た目
  └─ 右端 sheet を追加時の土台に

Markdown 生成 values
  ↓
template sheets へ書き込み
```

## 注意

- 数式、グラフ、図形、pivot、既存セル値の完全維持ではない
- 見た目の足場を借りる機能

## 画像内ラベル

- 「sheet-format source」
- 「values を載せる」
