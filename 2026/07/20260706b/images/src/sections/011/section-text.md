# セクション整理: 出力

## 主題

- 主出力は `.xlsx`
- stdout / stderr の役割を分ける
- 画像とリンク、sheet mode、miku-xlsx2md compatibility を整理

## 出力の役割

- XLSX: 主出力
- stdout metadata: version / help
- stderr diagnostics: usage error / runtime error

## 画像とリンク

- local PNG/JPEG/GIF: embedded image
- remote image URL: text reference
- missing image: text reference
- single Markdown link: Excel hyperlink
- mixed text with link: text

## Sheet mode

- single: 1 worksheet
- heading depth 1: `#`
- heading depth 2: `##`

## 吹き出し案

出力先、画像、リンク、sheet 分割を分けて考えると安全です…！
