---
title: 簡易RAG風Agent Skillsの作成 step3：蒸留Markdownでキャッシュする
description: miku-indexgen による索引だけでは残る本文読解コストを、蒸留した Markdown キャッシュでどう軽くできるかを扱う予定のドラフトです。
tags: "#生成AI #AIエージェント #AgentSkills #RAG #Markdown #GitHub #トークン消費 #技術エッセイ #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: TBD
---

# 簡易RAG風Agent Skillsの作成 step3：蒸留Markdownでキャッシュする

## メモ

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
- その Markdown を、`references/` 以下のキャッシュとして扱う
- 毎回多数の記事本文を読むのではなく、まず蒸留済み Markdown を読む
- 必要なときだけ元記事本文へ戻る
- トークン消費がどのくらい変わるかを見る

## 位置づけ

`index.json` は、どのファイルを見るかの地図。

蒸留 Markdown は、よく使う文脈を短くまとめたキャッシュ。

あの…地図だけでは、目的地の中身までは分かりません。step3 では、よく行く場所の案内メモを作る感じです。
