# 006 実行方式の選び方

## 主題

Node.js と Java の両方に対応し、利用者環境に合わせて backend を選べるようにする。

## 図解キーワード

- backend
- Node.js
- Java
- environment fit
- no silent fallback
- reproducibility

## 選択ルール

| 条件 | 選ぶもの |
| --- | --- |
| Java / jar / Maven | Java runtime |
| Node.js / JavaScript / `.mjs` | Node.js runtime |
| 指定なし | bundled Node.js CLI を優先 |
| `*-only` | 別 backend に黙って逃げない |

## 図解したい対比

```text
環境に合わせる
  Node.js OK
  Java OK

でも勝手に変えない
  reproducibility
```

## 吹き出し案

「選べます。でも勝手には変えません…」
