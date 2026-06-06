# グラレコ制作用整理テキスト

## 1. 大テーマ

```text
生成AI開発の Engineering は
「命令を書く」から
「AI が迷わず作業できる世界を設計する」へ
```

中心メッセージ:

- Prompt の時代から Context の時代へ
- AI agent は、repository / tools / memory / retrieval と一緒に動く
- モデル単体ではなく、外側の構造も作業品質を決める

## 2. Before / After

| Before | After |
|---|---|
| 良い prompt を書く | 探索しやすい世界を設計する |
| 1回の入力が中心 | 継続作業環境が中心 |
| Chat 中心 | Agent 中心 |
| 全文を読ませる | 必要部分だけ見せる |
| モデル性能依存 | 構造設計依存 |
| 人間向け repo | 人間 + AI agent 共存 repo |

## 3. Prompt Engineering と Context Engineering

```text
Prompt Engineering
  = AI にどう命令するか

Context Engineering
  = AI に何を見せるか
  = AI が参照する情報空間を設計する
```

対比:

| 項目 | Prompt | Context |
|---|---|---|
| 主対象 | 命令文 | 情報空間 |
| 主眼 | 書き方 | 見せ方 |
| 単位 | 1回の入力 | 継続作業環境 |
| 技術 | role / few-shot / XML | retrieval / tools / memory |

## 4. Context を供給する装置

```text
repository 全体
  ↓
README / docs / TODO
  ↓
retrieval / vector search / symbol search
  ↓
MCP / tool output / cache
  ↓
Agent Skills / memory
  ↓
AI agent が迷わず作業
```

役割:

| 要素 | 役割 |
|---|---|
| repository | AI の作業世界 |
| README | 入口 |
| docs | 設計思想・判断理由 |
| TODO | 再開の足場 |
| retrieval | 必要情報の抽出 |
| tool output | 観測結果 |
| memory | 長期知識 |
| Agent Skills | 手順・判断基準 |

## 5. 増えている Engineering 群

```text
Prompt Engineering
  命令文を設計

Context Engineering
  情報空間を設計

Retrieval Engineering
  必要情報の取り出し方を設計

Tool Engineering
  AI が使いやすい道具の契約を設計

Agent Engineering
  考える→実行→観測→修正のループを設計

Repository Engineering
  AI が作業しやすい repo 構造を設計
```

## 6. これから重要になりそうな概念

```text
context compression
  巨大情報を圧縮した地図にする

context routing
  作業内容に応じて必要 context だけ流す

hierarchical retrieval
  repo → module → file → symbol → line

repository memory
  設計思想・危険箇所・判断理由を残す

execution trace memory
  command / 修正 / test / failure history を残す

long-horizon planning
  長期タスクの現在地と次の一手を保つ
```

## 7. Repository Engineering の本質

```text
AI を直接賢くすることではなく
AI が迷わない構造を作ること
```

図解:

```text
Model
  x
Tools
  x
Memory
  x
Retrieval
  x
Context Engineering
  =
実際に作業できる AI agent
```

## 8. まとめ

- Prompt は大切だが、それだけでは足りない
- AI agent には、作業世界そのものの設計が必要
- README、docs、TODO、repository map、search tool、Agent Skills、memory、tool output は context 供給装置
- 生成AI開発は「命令文」から「環境設計」へ広がっている

吹き出し候補:

```text
「あ、あの…全体像はこんな感じです…！」
「Prompt だけではなく、Context も大事なのです…」
「AI が迷わない作業世界を作るのがポイントです…！」
```
