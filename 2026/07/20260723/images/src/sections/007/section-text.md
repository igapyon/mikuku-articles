# MCP と Agent Skills は、競合ではなく役割の違い

## 主題

- MCP と Agent Skill の優劣ではなく、運び方と役割が違う
- MCP は共通方式で tool を公開し、Agent Skill は CLI 実行と作業手順をまとめる
- 同じ公開実装を別の方法で AI agent へ渡す試み

## 図解キーワード

- 競合ではない
- MCP Server
- stdio／Streamable HTTP
- OAuth／toolset
- CLI-only
- 明示発火
- 承認／二重確認
- 共通の入口／手順書と安全係

## 関係・流れ・対比

| MCP Server | backlog-api-skills |
| --- | --- |
| MCP client へ tool を公開 | 同梱 Node CLI を必要時に実行 |
| stdio／Streamable HTTP | CLI-only |
| 共通の入口 | 発火・判断・確認・結果の読み方 |

## グラレコ構図案

- 左: MCP Server の接続ハブ
- 中央: 「優劣ではなく役割の違い」という等価な橋
- 右: Agent Skill の手順書・安全係カードとみくく
- みくくの表情・視線: 誤解をほどく真剣な表情で左右を見比べる
- 吹き出し: 「どちらも大切。役割が違うのです…」

## 正確性メモ

- MCP より Agent Skills が優れているという図にしない
- MCP 側の機能は Docker、npx、stdio、Streamable HTTP、OAuth、toolset 選択
- Agent Skill 側は CLI-only と人の確認 workflow
