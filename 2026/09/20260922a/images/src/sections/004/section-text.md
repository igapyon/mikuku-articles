# CLI や外部サービスを、Agent から扱うための14件

## 主題

- もう半分の14件は、個別の tool や service を Agent Skills として扱いやすくする専用リポジトリ
- miku-soft の CLI、Backlog API、記事参照用 sample など、用途ごとに分かれている
- `igapyon-miku-indexgen` や `igapyon-miku-text-bundle` のように、他の作業の見つけやすさや受け渡しを支えるものもある

## 図解キーワード

- 専用リポジトリ
- 14件
- CLI
- 外部 service
- `igapyon-backlog-api`
- `igapyon-miku-indexgen`
- `igapyon-miku-text-bundle`
- `mikuproject`
- `mikuscore`

## 関係・流れ・対比

```text
個別の tool / service
  ↓ 専用リポジトリに分ける
Agent Skill として扱いやすくする
  ├─ 日常的に使う: `igapyon-miku-indexgen`
  ├─ 間接的に効く: `igapyon-miku-text-bundle`
  └─ これから育てる: `mikuproject` / `mikuscore`
```

## 図解構造

- layout-family: layers
- primary-relation: 個別の tool や service を用途別の専用リポジトリへ分け、Agent から扱いやすい入口にする層構造

## グラレコ構図案

- 左: `tool / service` の小さな入口群。CLI、Backlog API、記事参照 sample の短いラベルを置く
- 中央: 最大の層構造。`専用リポジトリ 14件` を中心に、下から `tool / service`、中央に `Agent Skill`、上に `作業で使いやすい入口` と積む
- 右: 3つの状態カード `頻繁に使う`、`間接的に効く`、`これから育てたい`。代表例は `igapyon-miku-indexgen`、`igapyon-miku-text-bundle`、`mikuproject`、`mikuscore` など少数にする。みくくを右下へ置く
- みくくの表情・視線: 右側で仕組みがつながったことを説明する明るい表情。中央の層構造を見る。手は空にする
- 吹き出し: 「用途ごとに分けると、扱いやすくなります…」

## 正確性メモ

- 専用リポジトリは14件
- `igapyon-backlog-api`、`igapyon-miku-indexgen`、`igapyon-miku-text-bundle`、`mikuproject`、`mikuscore` は記事本文にある例
- 記事本文にない service 名、性能評価、利用回数は足さない

## 共通スタイル契約

- style-profile: mikuku-graphic-recording-v1
- 横長 3:2、左・中央・右の3領域、中央の層構造を最大化
- 背景は均一に明るく全面不透明。文字は濃色、カードや矢印だけ淡い色
- みくくは1人、物を持たず、短い吹き出しを1つ

## 変更（deviation）

- none
