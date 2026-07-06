# セクション整理: Exit code

## 主題

- Node.js 版と Java 版の exit code の意味
- automation で結果判定しやすくする

## 対応

| code | 意味 |
| --- | --- |
| 0 | success / help / version |
| 1 | conversion / file-system / I/O failure |
| 2 | invalid CLI usage |

## 図解

```text
CLI 実行
  ↓
0 = OK
1 = 処理失敗
2 = 使い方エラー
```

## 注意

- missing input
- missing `--out`
- parse error
- runtime error

## 吹き出し案

exit code を見ると、自動実行でも原因を分けやすいです…！
