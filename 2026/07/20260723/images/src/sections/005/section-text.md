# Agent Skill として、安全確認を前へ置く

## 主題

- 読み取りは既定で許可、作成・更新・削除は直前の人の承認が必要
- 破壊的・広範囲な操作は二段階目の確認を行う
- 認証情報と診断情報を限定して扱う

## 図解キーワード

- READ
- CREATE／UPDATE／DELETE
- 人の直前承認
- `--allow`
- 影響確認
- `--confirm-destructive`
- 環境変数
- safe diagnostics

## 関係・流れ・対比

```text
READ → 既定で許可

CREATE／UPDATE／DELETE
  ↓ 対象・operation・変更内容を提示
人の直前承認
  ↓ --allow
破壊的・広範囲？ ─ yes → 影響を再確認 → --confirm-destructive
```

## グラレコ構図案

- 左: READ と WRITE の分岐
- 中央: 承認から `--allow`、再確認への安全ゲートを大きく描く
- 右: API key は環境変数、診断は限定情報だけ、という盾カードとみくく
- みくくの表情・視線: 慎重な表情で中央の停止線を見る
- 吹き出し: 「進み方と、立ち止まる場所を決めます…」

## 正確性メモ

- 一度の承認で破壊的操作まで同時承認しない
- API key を会話へ貼る運用にしない
- `--verbose` でも本文、検索語、個人情報、error body、認証情報を出さない設計
