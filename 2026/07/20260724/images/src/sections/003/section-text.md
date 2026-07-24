# 一つの名前が、二つのプロジェクトになった

## 主題

- 当初は一つの `backlog-api-skills` に実行機能と Agent Skill 配布を収める想定
- みくくが過去の miku-soft の型から分割案を提案
- 人が提案を採用し、責務の異なる二つのプロジェクトになった

## 図解キーワード

- 一つの箱
- 責務を分ける
- `backlog-api`
- Node Core／CLI
- `backlog-api-skills`
- Agent Skill 配布
- 提案
- 人が採用

## 関係・流れ・対比

```text
backlog-api-skills（一つの構想）
          ↓ 分割案
┌────────────────┬────────────────────┐
│ backlog-api    │ backlog-api-skills │
│ 実行機能       │ runtime・使い方の配布 │
│ Node Core／CLI │ Agent Skill        │
└────────────────┴────────────────────┘
```

- 任せる = 型から具体案を出してもらう
- 決めてもらう = 無条件に採用する、ではない

## グラレコ構図案

- 左: 一つの大きな箱 `backlog-api-skills`
- 中央: 「責務が近すぎる？」という分岐とみくくの提案
- 右: 二つの明確な箱と「igapyon が採用」
- みくくの表情・視線: ドキドキしながら分割案を見る
- 吹き出し: 「役割を分けると、責務が見えやすくなります…！」

## 正確性メモ

- 分割案はみくくが提案し、igapyon が確認・採用
- `backlog-api` は Backlog API を利用する Node Core／CLI
- `backlog-api-skills` は runtime と使い方を Agent Skill として配る側
