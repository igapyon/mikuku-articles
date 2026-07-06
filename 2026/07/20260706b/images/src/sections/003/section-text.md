# セクション整理: 表現対応表

## 主題

- Markdown 側の表現が Excel workbook 側でどう表現されるか
- Node.js 版 v0.6.6 と Java 版 v0.6.5 の代表対応

## 図解

```text
Markdown 表現
  ↓
workbook model
  ↓
worksheet / row / cell / hyperlink / media / merge
```

## 代表対応

- heading → heading row / sheet split
- paragraph → worksheet row
- list → list row
- table → rows / cells
- code block → code row
- link → hyperlink
- local image → embedded media
- `[←M←]` / `[↑M↑]` → merge range

## 注意

- numeric-looking text は string cell
- formula-like text は native formula にしない

## 吹き出し案

どの Markdown が、Excel のどこへ行くかを見えるようにします…！
