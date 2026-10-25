# Backlog MCP から Agent Skill へ

## 主題

- Nulab さんの公開した Backlog MCP Server の実装を出発点にする
- MCP transport を外し、TypeScript ベースの Node Core／CLI へ変換
- CLI runtime と安全な作業手順を Agent Skill としてまとめる
- 「動く」だけでなく「いつ使う・どこで止まる」まで設計する

## 図解キーワード

- Nulab Backlog MCP Server
- 公開 tool handler
- backlog-api
- Node Core／CLI
- backlog-api-skills
- 明示発火
- 人の直前承認
- 二重確認
- CLI-only
- ベータ版

## 関係・流れ・対比

### 三層の変換

```text
Nulab Backlog MCP Server
公開された tool handler と API の振る舞い
                ↓ MCP transport を外す
backlog-api
TypeScript ベースの Node Core／CLI
                ↓ runtime と運用をまとめる
backlog-api-skills
明示発火・対象確認・安全規則・CLI 実行
```

### MCP と Agent Skill の役割

| MCP | Agent Skill |
| --- | --- |
| AI agent と外部サービスを「つなぐ」 | 道具を「どう扱うか」を伝える |
| stdio／Streamable HTTP | 同梱 Node CLI を必要時に実行 |
| tool を共通方式で公開 | 発火・判断・承認・結果確認を案内 |

### 変更操作の安全フロー

```text
明示発火
  ↓
対象と operation を確認
  ↓
人の直前承認
  ↓
--allow CREATE / UPDATE / DELETE
  ↓ 破壊的・広範囲なら
もう一度、影響を確認
  ↓
--confirm-destructive
```

## 役割分担・判断軸

| 要素 | 役割 |
| --- | --- |
| Nulab Backlog MCP Server | 上流となる公開実装 |
| backlog-api | MCP transport を外した Node Core／CLI |
| backlog-api-skills | Agent 向けの発火・確認・安全運用 |
| 環境変数 | `BACKLOG_DOMAIN` と `BACKLOG_API_KEY` を runtime へ渡す |
| `fields` | AI agent へ返す情報量を絞る |

- 読み取り: 既定で許可
- 作成・更新・削除: `--allow` と人の承認が必要
- 破壊的・広範囲な操作: 二段階目の確認が必要
- 発火: Skill 名や workflow が明示されたときだけ
- 現状: `v0.3.4`、Node.js 22 以降、通常 tool 58 個、ベータ版

## グラレコ構図案

- 左: Docker／`npx`／別 process の MCP Server と、「別 process は起動したくない」という出発点
- 中央: `Nulab MCP → backlog-api → backlog-api-skills` の三層変換を最も大きく配置
- 右: 安全フローの縦矢印と、左向きに図解を見るみくく
- 最も大きく見せる主図: 三層変換と「つなぐ MCP／扱い方を伝える Agent Skill」の役割対比
- みくくの表情・視線: 少し慎重な優しい表情で、中央の三層図と右下の安全確認を見つめる
- 吹き出し: 「あ、あの…動くだけでは、まだ足りなかったのです」

## 正確性メモ

- Nulab 公式 MCP Server と、非公式の派生プロジェクトを混同しない
- `backlog-api` と `backlog-api-skills` は MIT ライセンスのベータ版
- `v0.3.4`、Node.js 22 以降、上流 `v0.13.2`、通常 tool 58 個は記事記載値
- MCP より Agent Skills が優れている、という図にしない
- Docker だけが公式 MCP の起動方法であるように描かない
- 動作確認が十分ではなく、interface や workflow が変わる可能性を小さな注意ボックスで示す
