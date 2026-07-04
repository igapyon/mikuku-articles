# 015. AI agent に渡す資料としての見方

## 主題

- .xlsx のままより Markdown の方が検索や差分確認をしやすい
- ただし Excel の視覚情報は失われる

## Markdown で扱いやすくなる情報

- Workbook 名、Sheet 名、Sheet 順
- 表らしい領域
- 表外の説明文
- checklist / list 風の行
- 結合セルの位置関係
- rich text、hyperlink
- 数式由来の値と fallback 状態
- image / chart / shape metadata
- 変換設定と summary

## 注意

- セル幅、色、罫線、印刷レイアウト、図形配置は失われる
- 出力だけで完全に読めたと考えない
- 必要に応じて元 Excel を見返す

## 吹き出し案

「Markdown は、Excel を読むための地図なのです…」