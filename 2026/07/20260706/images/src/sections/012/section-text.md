# 012. 表検出 mode の見方

## 主題

- Excel で難しいのは、どこを表として見るか
- sheet の性質に合わせて mode を選ぶ

## mode 対比

| mode | 方針 | 向く sheet |
| --- | --- | --- |
| balanced | 汎用 heuristic | 通常の一覧表、設計書、台帳 |
| border | 罫線重視 | 罫線で表が明確 |
| planner-aware | 過剰な表検出を抑制 | Excel 方眼、計画表、カレンダー |

## 選び方

```text
まず balanced
  ↓
拾われすぎる / 拾われない
  ↓
border または planner-aware
```

## 注意

- Markdown はセル座標や見た目を保つ形式ではない
- 表として切り出しすぎると読みにくくなる

## 吹き出し案

「表にしすぎても、読みにくくなることがあります…」