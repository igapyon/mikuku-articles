---
title: 簡易RAG風Agent Skillsの作成 step3：索引の前後でトークン消費を比べる
description: miku-indexgen を足す前後で、同じ依頼をしたときのトークン消費、実行時間、AI agent が発行する探索コマンドの変化を観察するためのドラフトです。
tags: "#生成AI #AIエージェント #AgentSkills #RAG #Markdown #GitHub #mikuindexgen #トークン消費 #技術エッセイ #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: TBD
---

# 簡易RAG風Agent Skillsの作成 step3：索引の前後でトークン消費を比べる

あ、あの…今回は、`miku-indexgen` を Agent Skill の参照データとして足したときに、AI agent の探索がどう変わるかを見たいです。

ただ、その前にひとつ地味な準備があります。

チェックアウト直後のリポジトリには、比較対象にする raw corpus がまだありません。そこで、まずは記事データを `references/raw/mikuku-articles` に clone しておく必要があります。

今までは、この準備を人間が思い出して実行する感じでした。でも、それだと比較作業に入るたびに「あれ、最初に何を置くんでしたっけ…」となりやすいです。

なので step3 では、完全自動化の前に、まずルートの `README.md` に準備手順を書いておくところから始めます。

## step3 でやりたいこと

step2 では、`miku-indexgen` を足して `references/index/mikuku-articles/index.json` と `index.md` を作るところまでに絞る。

step3 では、その前後比較を扱う。

見たいものは次の 2 つ。

- トークン消費がどう変わるか
- AI agent が発行するコマンドや探索の仕方がどう変わるか

ただし、比較を始める前に、参照用の raw corpus が同じ場所にあることを固定しておく。

```text
references/raw/mikuku-articles
```

ここがそろっていないと、索引の有無ではなく、手元の作業環境の違いを比べてしまうことになる。

うぅ…ここはとても地味ですが、比較の土台としてはかなり大事です。

## チェックアウト直後の準備を README に書く

チェックアウト直後に必要な準備は、ルートの `README.md` に書いておく。

```sh
mkdir -p references/raw
git clone https://github.com/igapyon/mikuku-articles.git references/raw/mikuku-articles
```

すでに clone 済みの場合は、clone し直すのではなく更新する。

```sh
git -C references/raw/mikuku-articles pull --ff-only
```

`references/raw/` は作業用データなので、Git には入れない。リポジトリに入れるのは、準備手順と、必要なら生成された索引や Agent Skill 側の説明だけにする。

ここまでを README に置いておくと、次からは AI agent に対して次のように頼みやすくなる。

```text
README.md を読んで、Agent Skills RAG 比較用の準備を進めてください。
```

まだ完全自動ではないけれど、毎回の口頭説明を減らせる。半自動化の最初の一歩としては、まずこのくらいが扱いやすいかな、と思います。

## 比較に使うプロンプト

比較に使うプロンプトは、step1 と同じものにする。

```text
このリポジトリの `SKILL.md` を読んで、その指示に従ってください。
Agent Skills に関係する既存記事を探してください。
```

プロンプトを変えすぎると、`miku-indexgen` の効果なのか、依頼文の効果なのか分からなくなる。

ただし、実験前の環境準備としては、README に書いた raw corpus の clone 手順を実行しておく。比較プロンプトそのものと、比較前の準備手順は分けて扱う。

## 足す前の記録欄

```text
足す前:
  モデル:
  プロンプト:
  実行時間:
  トークン消費:
  主に発行されたコマンド:
  読まれた主なファイル:
  観察メモ:
```

足す前のイメージ。

```text
README.md を読む
SKILL.md を読む
references/raw/mikuku-articles があるか確認する
記事候補をローカル検索する
候補が多ければ、タイトル・タグ・ファイル名で絞る
必要そうな Markdown を読む
結果をまとめる
```

## 足した後の記録欄

```text
足した後:
  モデル:
  プロンプト:
  実行時間:
  トークン消費:
  主に発行されたコマンド:
  読まれた主なファイル:
  観察メモ:
```

足した後のイメージ。

```text
README.md を読む
SKILL.md を読む
references/index/mikuku-articles/index.md または index.json を読む
索引から候補を絞る
必要そうな Markdown を読む
結果をまとめる
```

## 比較表

```markdown
| 条件 | トークン消費 | 実行時間 | 主な入口 | 主な探索コマンド | 読まれた本文ファイル数 | 観察 |
|---|---:|---:|---|---|---:|---|
| miku-indexgen なし |  |  | raw corpus |  |  |  |
| miku-indexgen あり |  |  | index + raw corpus |  |  |  |
```

## 注意点

トークン消費の数字は、絶対的なベンチマークではなく、同じ手元環境での前後比較として扱う。

同じプロンプトでも、モデル、環境、会話履歴、キャッシュ、ツール実行結果の扱いで変わる。

減るかもしれない。あまり変わらないかもしれない。場合によっては、`index.md` を読むぶんだけ一時的に増えることもあるかもしれない。

見たいのは、きれいな結論ではなく、同じ依頼をしたときに AI agent の探索の仕方がどう変わるか。

## コマンドは変わるのか

step1 の素の状態では、AI agent は記事候補を探すために、ローカル検索やディレクトリ確認を直接使っていた。

`miku-indexgen` を足した後は、理想的には次のように変わってほしい。

- まず `SKILL.md` を読む
- 次に `references/index/mikuku-articles/index.md` または `index.json` を読む
- そこで候補を絞る
- 必要な記事 Markdown だけを読む

つまり、ユーザーが発行するプロンプトは同じでも、AI agent の内部的な探索コマンドは変わるかもしれない。

そして、その観察の前段として、`README.md` に「raw corpus はここに置く」と書いておく。

人間が毎回説明するのではなく、リポジトリの中の文書を AI agent が読んで準備できるようにする。これも、広い意味では Agent Skills 的な作業の一部なのかもしれません。

## ここから測定に進む

次にやることは、同じプロンプトを使って、索引なし・索引ありの 2 回を記録すること。

そのとき、見るものは数字だけではない。

- どのファイルを入口にしたか
- `rg` や `find` をどのくらい使ったか
- いきなり本文を読みに行ったか
- 先に `index.md` や `index.json` を読んだか
- 候補を絞ってから本文に入れたか

トークン消費が少し減るだけなら、それはそれで嬉しい。でも、もっと見たいのは、AI agent の迷い方が変わるかどうかです。

索引があることで、最初の探索が少し落ち着くなら、それは RAG というほど大げさではなくても、実用上はかなり意味があるはずです。

あの…小さな地図があるだけで、AI agent の歩き方が少し変わる。今回はその変化を、なるべく手元の記録として残してみたいです。
