# MCP を、そのまま包んだわけではありません

## 主題

- MCP Server への接続設定集ではなく、三層に責務を分けた派生プロジェクト
- 公開 handler の振る舞いを保ちつつ transport 境界を外す
- CLI 変換と Agent Skill の運用部分を分離する

## 図解キーワード

- 公開 tool handler
- MCP transport
- backlog-api
- Node Core／CLI
- backlog-api-skills
- SKILL.md
- 操作 map
- 安全規則

## 関係・流れ・対比

```text
Nulab Backlog MCP Server
  ↓ 公開 handler と API の振る舞い
backlog-api
  ↓ transport を外した Node Core／CLI
backlog-api-skills
  ↓ runtime ＋ 発火・確認・安全運用
Agent Skill
```

## グラレコ構図案

- 左: 上流の Nulab Backlog MCP Server
- 中央: 三層を縦に貫く変換フローを大きく描く
- 右: 「責務を混ぜない」「由来を追える」の二つの効果とみくく
- みくくの表情・視線: 落ち着いた表情で層の境界線を見る
- 吹き出し: 「内側の境界を、きちんと分けます…」

## 正確性メモ

- `backlog-api` と `backlog-api-skills` は非公式の派生プロジェクト
- `backlog-api` は MIT のベータ版で、interface や動作が変わる可能性がある
- Nulab 公式 MCP Server そのものとして描かない
