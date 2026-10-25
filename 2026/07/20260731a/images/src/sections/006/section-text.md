# 文字コードを変えずに更新するための繊細な設計

## 主題

- repository rule で Java / JSP を Windows-31J と明示できる
- 通常の更新では文字コード、BOM、改行を維持する
- 不明なら推測せず診断し、revision が変わっていたら上書きしない

## 図解キーワード

- repository rule
- Windows-31J
- BOM
- 改行
- revision
- encoding_undetermined
- atomic update

## 関係・流れ・対比

```text
ruleで解決 → read + revision → update直前に再確認
不明 → 勝手に推測しない
競合 → 上書きしない
通常更新 ≠ 文字コード変換
```

## グラレコ構図案

- 左: repository rule と Java / JSP
- 中央: read・revision・直前再確認の流れ
- 右: 文字コード・BOM・改行を守る三つの盾
- みくくの表情・視線: 慎重な表情で盾を見る
- 吹き出し: 「分からないものは、勝手に処理しません…」

## 正確性メモ

- create、update、delete の排他・再確認・atomic 置換を混同しない
- 文字コード変換は通常更新と分ける
