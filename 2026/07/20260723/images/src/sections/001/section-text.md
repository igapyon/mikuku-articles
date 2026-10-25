# はじめに

## 主題

- Nulab さんの Backlog MCP Server を使ってみたい、という素朴な出発点
- 別 process の MCP Server を起動せず、Node Core／CLI と Agent Skill へ変換する発想
- MCP は「つなぐ」、Agent Skill は「どう扱うかを伝える」

## 図解キーワード

- 公式 MCP
- Docker／npx／Node.js
- 別 process
- MCP transport
- Node Core／CLI
- Agent Skill

## 関係・流れ・対比

```text
公式 MCP を使いたい
  ↓ でも別 process は起動したくない
公開 source code
  ↓ MCP transport を通さない形へ
Node Core／CLI ＋ Agent Skill
```

## グラレコ構図案

- 左: Docker／npx／Node.js から MCP Server を起動する入口
- 中央: 「別 process は起動したくない」という気づきと変換矢印
- 右: 「MCP＝つなぐ」「Agent Skill＝扱い方」の二枚カードとみくく
- みくくの表情・視線: 驚きと好奇心のある表情で中央の変換を見る
- 吹き出し: 「ちょっと Agent Skill にしてみたいな…！」

## 正確性メモ

- Docker だけでなく `npx` と Node.js の起動方法もある
- GPT-5.6 Sol Medium への驚きは本文にあるが、図の中心は変換の発想に置く
- MCP と Agent Skill は役割が少し違う、と表現する
