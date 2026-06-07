# 状態の変化を書いてみる グラレコ整理

- 主題: `stateDiagram-v2` で注文状態の変化を書く
- Draft
- Submitted
- Approved
- Rejected
- 修正して Draft へ戻る
- Approved で終了

```text
開始
 ↓
Draft → Submitted → Approved → 終了
            ↓
         Rejected
            ↓
          Draft
```

キーワード:
- stateDiagram-v2
- 状態
- 遷移
- 開始
- 終了

吹き出し:
「いま何の状態で、次にどこへ進めるかを見るのです…」

