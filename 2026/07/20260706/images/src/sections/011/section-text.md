# 011. output mode の見方

## 主題

- Excel の表示値と内部値の差を見る
- display / raw / both を使い分ける

## mode 対比

| mode | 見方 | 向く確認 |
| --- | --- | --- |
| display | 表示値寄り | 普通に読む、AI agent に渡す |
| raw | 内部値寄り | 型や元値の確認 |
| both | 表示値 + raw 差分 | ズレ確認 |

## 重要ポイント

- 日付、数値、パーセント、桁区切り、数式で差が出やすい
- 通常は display が扱いやすい
- 差が重要なら both

## 図解

```text
Excel cell
  ├─ display value: 人間が見る値
  └─ raw value: 内部の値
```

## 吹き出し案

「見えている値と中の値は、同じとは限らないのです…」