# セクション整理: 基本コマンド

## 主題

- 最小コマンドは入力 Markdown と `--out`
- sheet 分割する場合は `--sheet-mode heading`

## コマンド要素

- Node.js: `node miku-md2xlsx-0.6.6.mjs input.md --out output.xlsx`
- Java: `java -jar miku-md2xlsx-java-0.6.5.jar input.md --out output.xlsx`
- heading mode
- heading depth 2

## 図解

```text
input.md + --out output.xlsx
```

## 注意

- `--out` は必須
- XLSX bytes を stdout へ流す CLI として扱わない

## 吹き出し案

まずは input.md と --out output.xlsx の最小形からです…！
