# 少しだけ技術の言葉に戻す

## 主題

比喩でつかんだ輪郭を MCP の用語へ対応させる。

## 対応表

| 比喩 | MCP 用語 | 役割 |
| --- | --- | --- |
| 魔法陣 | MCP | 外部へ手を伸ばす仕組み |
| 受付・場 | MCP server | tool / resource を公開 |
| 妖精さんのお仕事 | tool | 実行できる処理 |
| 資料や記録 | resource | 読みに行ける情報 |
| 術式 | tool schema | 渡す材料の形 |

## 図解

```text
MCP server
  ├─ tool
  ├─ resource
  └─ tool schema

client / agent が分かる形で公開
```

## 伝えたいこと

細かい仕様の前に「魔法陣でお願いを届ける」絵を持つと迷子になりにくい。
