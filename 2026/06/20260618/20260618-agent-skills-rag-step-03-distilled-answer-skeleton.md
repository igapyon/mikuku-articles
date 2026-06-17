---
title: 簡易RAG風Agent Skillsの作成 step3：蒸留 Markdownで回答の骨格を作る
description: miku-indexgen による索引の次に、記事群の見方を抽出した蒸留 Markdown を置き、AI agent の回答の骨格を安定させる実践型技術エッセイです。
tags: "#生成AI #AIエージェント #AgentSkills #RAG #Markdown #GitHub #トークン消費 #技術エッセイ #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: 2026-06-18
---

# 簡易RAG風Agent Skillsの作成 step3：蒸留 Markdownで回答の骨格を作る

## メモ

この記事では、記事群から見方や主張を短く抽出した Markdown を、蒸留 Markdown と呼びます。実装上のディレクトリ名に合わせて、`distilled Markdown` とも呼びます。

step2 では、`miku-indexgen` を足して `index.json` を入口にした。

結果として、探索の入口は変わった。

```text
index.json なし: 平均 約 110.6K used
index.json あり: 平均 約 82.4K used
```

ただし、揺れは大きかった。

理由は、今回の質問が「記事を探す」だけではなく、「記事群の主張や考え方を整理する」ものだったから。

つまり、最終的には本文 Markdown を読む必要がある。

step3 では、ここに蒸留 Markdown を足す。

## 扱う予定のこと

- Agent Skills 関連記事の要点を、短い Markdown に蒸留する
- その Markdown を、`references/distilled/` 以下の読書メモとして扱う
- 毎回多数の記事本文を読む前に、まず蒸留 Markdown で回答の骨格を作る
- 必要なときだけ元記事本文へ戻る
- トークン消費だけでなく、回答の見方がどのくらい安定するかを見る

最初に作る蒸留 Markdown の候補は、次の4本にする。

```text
references/distilled/
  about-agent-skills.md
  agent-skills-directory-structure.md
  agent-skills-rag-pattern.md
  agent-skills-token-efficiency.md
```

それぞれの役割は、次のように分ける。

```text
about-agent-skills.md:
  思想。
  mikuku-articles の記事群では、Agent Skills をどう捉えているか。

agent-skills-directory-structure.md:
  構造。
  SKILL.md、references/、raw/、distilled/、index.json などをどう分けるか。

agent-skills-rag-pattern.md:
  実験。
  raw、index.json、蒸留 Markdown を使った簡易RAG風 Agent Skill の作り方。

agent-skills-token-efficiency.md:
  運用。
  なぜ全部読ませず、読む順番を作るのか。
```

## 位置づけ

`index.json` は、どのファイルを見るかの地図。

蒸留 Markdown は、記事群の見方を短くまとめた読書メモ。

あの…地図だけでは、目的地の中身までは分かりません。step3 では、よく行く場所の案内メモを作り、AI agent が回答するときの骨格を先に持てるようにする感じです。
