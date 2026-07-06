# セクション整理: 対応範囲外または限定対応

## 主題

- `miku-md2xlsx` は完全な帳票復元ツールではない
- できる範囲と、対象外の範囲を明確に分ける

## 対比

```text
対象: Markdown 構造 → workbook 土台
対象外: Excel 固有の完成帳票復元
```

## 対象外

- pixel-perfect layout
- original cell addresses
- detailed styles
- native formula
- native chart / shape / SmartArt
- remote image download
- full round-trip

## 限定対応

- column hints
- merge markers
- local image
- `<ins>` / `<br>`

## 吹き出し案

魔法の完全復元ではなく、構造を戻すための小さな出口です…！
