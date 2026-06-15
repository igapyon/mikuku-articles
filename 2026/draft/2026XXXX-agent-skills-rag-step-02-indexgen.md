---
title: Agent Skillsで軽いRAG風の知識参照を作る実践型技術エッセイ step2：miku-indexgenで索引入口を強くする
description: step01で作った最小構成の Agent Skill に、miku-indexgen による index.json / index.md 生成を加え、記事データをより現実的に参照しやすくするためのチューニングを整理するドラフトです。
tags: "#生成AI #AIエージェント #AgentSkills #RAG #Markdown #GitHub #mikuindexgen #技術エッセイ #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: TBD
---

# Agent Skillsで軽いRAG風の知識参照を作る実践型技術エッセイ step2：miku-indexgenで索引入口を強くする

## メモ

step01 では、最小構成の `SKILL.md` と `.gitignore`、そして `references/raw/mikuku-articles/` の実データだけで、素の生成AI / AI agent がどこまで RAG 的に動くかを確認した。

step02 以降では、もう少し現実的に使いやすくするためのチューニングへ進む。

## 連作の見取り図

```text
step1:
  素の RAG 的 Agent Skills を作る
  skill-creator で器を作り、references/raw/ に記事データを置く

step2:
  miku-indexgen を投入する
  raw の内容から index.json / index.md を生成して、読む前の入口を強くする
  消費トークン数が減るかどうかを観察する

step3:
  記事構造を把握させる
  公開済み記事と下書き記事の関係を AI agent に読ませる

step4:
  蒸留する
  毎回読むべき短いガイドやルーティングメモを作る
```

## タグ運用メモ

この連作では各 step ごとに GitHub でタグを打つ。

記事を読みながら手元で再現するとき、どの時点のリポジトリ状態なのかが分からなくなると困るから。

想定タグ:

```text
step1-raw-agent-skill
step2-miku-indexgen
step3-structure-map
step4-distilled-guide
```

各記事は、対応するタグの状態を前提にする。

## なぜ mikuku-articles の記事を使うのか

step01 では、`mikuku-articles` の記事データを題材にした。

いちばん現実的な理由は、差し当たり、私が自由に扱える題材データがこれだったから。

公開済み記事と下書きがあり、量もそれなりにあり、内容も自分たちの管理下にある。RAG 的な参照実験をするとき、権利や公開範囲に気を取られずに試せるデータであることは、かなり大事。

そして、もうひとつの理由として、技術的にも題材としてちょうどよかった、という面がある。

`mikuku-articles` は、単なる記事置き場ではない。

そこには、みくく担当の記事、Agent Skills 関連の記事、生成AI・MCP・CLI・Markdown・miku-soft 関連の観察、公開済み記事、下書きが入っている。

つまり、AI agent にとっては大きな文脈の塊。

## 記事以外をどう扱うか

`mikuku-articles` には、記事本文だけではなく、画像や画像生成用のテキスト、README、TODO、docs、index.json、運用メモもある。

step01 ではそこまで広げず、文脈対象は記事に絞った。

対象を広げすぎると、最初の実験で何が効いているのか分かりにくくなるため。

step02 以降では、index、docs、補助テキストなどをどこまで入口や文脈として扱うかを検討する。
