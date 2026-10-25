# セクション別グラレコ制作用整理テキスト

## 見出し

TODO.md は、現在地を保つ

## 主題

`TODO.md` はAIエージェントと人間が現在地を取り戻すための作業状態ファイル。

## 図解キーワード

- AI Agent Current Tasks
- Tasks
- Blockers
- Retry Log
- 次の一手
- 作業再開
- 3回同じ失敗で停止
- 細かすぎない
- 大きすぎない

## 役割分担

| 項目 | 役割 |
| --- | --- |
| Tasks | 今やること |
| Blockers | 詰まり |
| Retry Log | 繰り返し失敗の記録 |

## 構図

```text
作業開始 → TODOを読む
作業中   → 状態を更新
詰まる   → Blockers / Retry Log
再開時   → 現在地へ戻る
```

