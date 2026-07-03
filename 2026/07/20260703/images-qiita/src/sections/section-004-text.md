# 004 変換ロジックはこのリポジトリに抱え込まない

## 主題

`miku-ms-office-skills` は変換本体ではなく、routing と runtime と policy をまとめる workflow adapter。

## 図解キーワード

- workflow adapter
- routing
- runtime discovery
- policy
- upstream converter

## 役割分担

| 要素 | 役割 |
| --- | --- |
| miku-ms-office-skills | 選ぶ、案内する、制約を伝える |
| upstream converter | 実際に変換する |

## 図解したい構造

```text
Agent Skill
  ├─ routing
  ├─ runtime discovery
  └─ execution policy

upstream converter
  └─ conversion behavior
```

## 吹き出し案

「変換本体は upstream に任せます…」
