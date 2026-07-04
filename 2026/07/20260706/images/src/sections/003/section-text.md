# 003. 表現対応表

## 主題

- Excel 側の表現が Markdown 側でどう出るか
- 変換結果を読むための対応表

## 代表的な対応

| Excel 側 | Markdown 側 |
| --- | --- |
| workbook | combined Markdown |
| worksheet | `## Sheet:` |
| 表らしいセル範囲 | pipe table |
| 表外セル群 | paragraph / list |
| 結合セル | `[←M←]` / `[↑M↑]` |
| hyperlink | Markdown link |
| comment | Comments section |
| image / chart / shape | metadata と asset |

## 表検出の考え方

```text
seed cell
  ↓
連結成分
  ↓
外接矩形
  ↓
罫線・密度・header らしさで score
```

## 注意

- Excel table 定義だけで Markdown table は決まらない
- 表と地の文の境界は曖昧
- summary と score で確認しやすくする

## 吹き出し案

「表っぽさは、罫線だけでは決めないのです…」