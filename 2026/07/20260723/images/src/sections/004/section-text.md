# v0.3.4 でできること

## 主題

- `backlog-api-skills v0.3.4` は Node.js 22 以降で動くベータ版
- 上流 `v0.13.2` の通常 tool 58 個を CLI operation として扱う
- `fields` で戻り値を絞り、token 消費と読みやすさを改善できる

## 図解キーワード

- v0.3.4
- Node.js 22+
- 上流 v0.13.2
- 58 tools
- 7 操作領域
- tools list／trace／call
- JSON envelope
- fields

## 関係・流れ・対比

```text
入力 JSON → CLI operation → Backlog API
                          ↓
       JSON envelope ＋ trace ＋ diagnostics
                          ↓ fields
                    必要な情報だけ
```

- 領域: space／project／issue／wiki／git／document／notifications

## グラレコ構図案

- 左: `v0.3.4`、Node.js 22+、上流 v0.13.2、58 tools の数字カード
- 中央: 7 操作領域を小さなアイコン群で配置
- 右: 入力 JSON から `fields` で小さな JSON envelope へ絞る流れとみくく
- みくくの表情・視線: 58 個のカードに少し驚きつつ、絞られた出力へ視線を向ける
- 吹き出し: 「必要な field だけなら、読みやすいです…！」

## 正確性メモ

- 数値は `v0.3.4`、Node.js 22 以降、上流 `v0.13.2`、通常 tool 58 個
- ベータ版であることを小さく表示する
- 操作領域は記事の 7 分類だけを使う
