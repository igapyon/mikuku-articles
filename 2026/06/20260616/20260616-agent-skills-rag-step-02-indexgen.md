---
title: 簡易RAG風Agent Skillsの作成 step2：miku-indexgenを足す
description: step1で作った最小構成の Agent Skill に miku-indexgen の索引を足し、AI agent が記事本文へ向かう前に軽い地図を見られるようにする実践型技術エッセイです。
tags: "#生成AI #AIエージェント #AgentSkills #RAG #Markdown #GitHub #mikuindexgen #技術エッセイ #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: 2026-06-16
---

# 簡易RAG風Agent Skillsの作成 step2：miku-indexgenを足す

## はじめに

この記事は、みくくが担当します。あ、あの…よろしくお願いします。

前回の step1 では、`SKILL.md` と `references/raw/` に置いた `mikuku-articles` の記事データだけで、AI agent がどのくらい RAG っぽく動けるのかを見ました。

結果として、かなり素朴な構成でも、Agent Skills に関係する記事を探し、記事群の主張まで整理できました。うぅ…あれは、書いている私にとってもけっこう驚きでした。

ただし、step1 の形には課題もあります。AI agent は、必要な記事を探すために、まずローカルのファイル群を探索します。記事が増えれば、探索の時間も、読み込む候補も、トークン消費も増えていくはずです。

そこで step2 では、やることをひとつだけ足します。

ファイルへの索引の追加です。

ここで使う `miku-indexgen` は、みくくが作ったファイル索引生成ツールです。

あの…今回は、まだ蒸留もしません。ルーティング用の手書きガイドも増やしません。まずはきれいな状態で作業用リポジトリを checkout し、README.md に記事データの置き方を書き、`miku-indexgen` をもちいてファイルへの索引を作ります。そのうえで、同じプロンプトを投げたときの動きとトークン消費を比べます。

## 今回のゴール

今回のゴールは、step1 の Agent Skill に `miku-indexgen` の索引を足すことです。

この記事では、次の3点に絞ります。

- `miku-indexgen` をもちいて、ファイルへの索引を作る
- `SKILL.md` に、まず索引を見るように追記する
- 索引なし、索引ありで、同じプロンプトを実行して比べる

ここで大事なのは、Agent Skill の中に記事本文を貼り込むのではなく、記事本文へ向かうための地図を足す、ということです。

ぱたぱた…step1 で棚を作ったなら、step2 ではその棚に最初の地図を置く感じです。

## 今回の測定の流れ

今回の流れは、次のようにします。

```text
1. step01-01 を checkout する
2. README.md を作る
3. README.md に従って references/raw/mikuku-articles を配置する
4. index.json がない状態で、同じプロンプトを実行する
5. この時点の表示を、miku-indexgen 適用前の基準値として記録する
6. miku-indexgen を適用してリポジトリ直下に index.json を生成する
7. SKILL.md に index を先に見る指示を追加する
8. まったく同じプロンプトをもう一度実行する
9. トークン消費と探索の流れがどう変わったかを見る
```

この順番にしておくと、`miku-indexgen` を足す前と後で、ユーザー側の依頼文を変えずに比べられます。

あの…比較としては小さいです。でも、同じプロンプトのまま、AI agent がどこから見に行くかが変わるなら、それはかなり大事な変化です。

## step01-01 タグを checkout する

step2 では、いったん作業用リポジトリをきれいな状態で checkout するところから始めます。

step1 の作業中には、`references/raw/` に記事データを置いたり、手元でいろいろ試したりしました。あの…その状態のまま進めることもできます。でも、記事として手順を残すなら、いったん新しく checkout した状態から始めたほうが、どこから何が増えたのか分かりやすくなります。

ここでは、step1 が終わった時点のタグとして `step01-01` を使います。

次のように作業用リポジトリを取得し、`step01-01` タグを checkout します。

```bash
git clone https://github.com/igapyon/mikuku-articles-rag-skill.git
cd mikuku-articles-rag-skill
git checkout step01-01
```

この `step01-01` が、step1 の作業が終わった時点の状態です。この時点では、Agent Skill 本体としては `SKILL.md` と `.gitignore` があるだけです。`references/raw/` の中身は Git 管理外なので、checkout 直後には記事データは入っていません。

うぅ…ここが少しだけ面倒です。でも、参照データを Git 管理外にした以上、記事データをどう置くかの手順は、どこかに書いておく必要があります。

## しかたなく README.md を作る

そこで、`README.md` を作ります。

本当は、今回の主役は `SKILL.md` と `references/` です。README.md を厚くしたいわけではありません。けれど、checkout した人が最初に見る場所としては、やはり README.md が自然です。

あの…しかたなく、という言い方は少し雑かもしれません。でも気持ちとしては、README.md に大きな設計思想を書くのではなく、最低限の復元手順だけを置く、という感じです。

README.md には、ここでは次のように書きました。

````markdown
# mikuku-articles-rag-skill

This Agent Skill reads article Markdown from a local copy of
`igapyon/mikuku-articles`.

## Prepare article data

The article corpus is not committed to this repository.
Clone it under `references/raw/` before using the skill.

```bash
mkdir -p references/raw
git clone https://github.com/igapyon/mikuku-articles.git references/raw/mikuku-articles
```

## Generate index

After preparing the raw article data, generate an index with `miku-indexgen`.

```bash
java -jar ../igapyon-agent-skills/lib/miku-indexgen-1.5.1.jar \
  --input-directory .
```
````

ここで README.md に書きたいのは、利用者向けの長い説明ではありません。

まず `references/raw/mikuku-articles` を作る。次に `miku-indexgen` でリポジトリ直下の `index.json` を作る。その復元手順だけです。

この README.md があると、checkout 直後の空っぽの `references/` を見ても、何を置けばよいか分かりやすくなります。AI agent にとっても、人間にとっても、最初の足場になります。

## miku-indexgen で索引を作る

索引を作る前に、まず同じプロンプトを一度実行しておきました。

```text
このリポジトリの `SKILL.md` を読んで、その指示に従ってください。
Agent Skills に関係する既存記事を探してください。
これら記事では、Agent Skills に対してどのような主張や考え方を持っているの？
```

この時点では、まだリポジトリ直下の `index.json` はありません。つまり、AI agent は `SKILL.md` と `README.md` を読んだあと、`references/raw/mikuku-articles` の記事群を直接探しに行くことになります。

最初の計測では、画面表示上のトークン消費は `103K used` でした。

ただし、あとで確認すると、記事リポジトリ側の `README.md` と `index.json` が処理に混ざっていました。今回の step2 では、記事本文を対象にした状態で `index.json` ありなしを見たいので、`references/raw/mikuku-articles` 側の `README.md` と `index.json` を除外して、あらためて計測し直しました。

あの…ここでは、この数字を厳密なベンチマークとしては扱いません。`miku-indexgen` を足す前の基準値として置いておきます。次に索引を作り、まったく同じプロンプトをもう一度実行して、動きがどう変わるかを見るためです。

考え方は単純です。`references/raw/mikuku-articles` の中身を毎回いきなり探すのではなく、先に軽い地図を作っておきます。

実際には、次のプロンプトで `miku-indexgen` を実行しました。

```text
igapyon-miku-indexgen スキルを使用して、現在のリポジトリ直下を対象に index.json を生成してください。
```

ここで使っているのは、`igapyon-miku-indexgen` スキルです。手で `index.json` を書くのではなく、スキル経由で `miku-indexgen` を実行して生成します。このスキルのダウンロード元は後述します。

この実行では、生成物はリポジトリ直下の `index.json` になります。

```text
mikuku-articles-rag-skill/
├── SKILL.md
├── README.md
├── .gitignore
├── index.json
├── references/
│   └── raw/
│       └── mikuku-articles/
```

`references/raw/` は、step1 と同じく Git 管理外のままとします。一方で、リポジトリ直下の `index.json` は Agent Skill 側の参照入口として扱います。

スキル使用ではなく記事中のコマンドとして実現するなら、`mikuku-articles-rag-skill` フォルダにいる前提で、たとえば次のようになります。

```bash
java -jar ../igapyon-agent-skills/lib/miku-indexgen-1.5.1.jar \
  --input-directory .
```

手元の環境に `miku-indexgen` の別の実行方法がある場合は、それに合わせます。ここで重要なのは、リポジトリ直下を対象にして `index.json` を生成することです。

うぅ…`index.json` を手で編集しないことも大事です。索引は生成物なので、必要になったら `miku-indexgen` を再実行して更新します。

## raw と index の役割を分ける

ここで、`raw` と `index` の役割を分けておきます。

```text
references/raw/mikuku-articles:
  GitHub から取得した実データ。
  記事本文 Markdown の置き場。
  step1 と同じく Git 管理外にする。

index.json:
  miku-indexgen が生成した索引。
  AI agent が最初に見る入口。
  Agent Skill 側の参照データとして扱う。
```

`index.json` は、記事本文の代わりではありません。あくまでも、どの記事を読みに行くかを選ぶための入口です。

あの…地図があっても、本文を読まなくてよいわけではありません。地図を見て、必要な場所へ行くためのものです。

## SKILL.md に索引入口を足す

索引を作っただけでは、AI agent が必ずそこを見るとは限りません。

そこで `SKILL.md` に、まず索引を入口として確認する、という指示を足します。

このとき、次のプロンプトを与えました。

```text
ファイルを探す際には、SKILL.md が index.json を最初に見るようにしてください。
```

あの…少し短い依頼です。でも、この短い依頼で、Agent Skill の探索順序を変えようとしています。raw corpus をいきなり探すのではなく、まず `index.json` を見るようにする、という変更です。

足す内容のイメージは、次のようなものです。

```markdown
## Index Guidance

- If `index.json` exists, inspect it before searching the raw corpus.
- Use the generated index to choose candidate article Markdown files.
- After choosing candidates, read the actual article Markdown under `references/raw/mikuku-articles`.
- Do not answer from the index alone when the user asks about article content.
```

ここでやりたいのは、AI agent に「まず地図を見て、それから本文へ行く」流れを作ることです。

この追記で、Agent Skill の構成は少しだけ変わります。

```text
step1:
  SKILL.md
  raw corpus

step2:
  SKILL.md
  index.json
  raw corpus
```

うぅ…増えたのは小さな索引だけです。でも、この小さな入口があることで、AI agent がいきなり広い raw corpus を探しに行かず、まず地図から候補を選べるようになります。

## 同じプロンプトをもう一度実行する

`index.json` を生成し、`SKILL.md` に「まず `index.json` を見る」という指示を足した状態で、もう一度まったく同じプロンプトを実行しました。

```text
このリポジトリの `SKILL.md` を読んで、その指示に従ってください。
Agent Skills に関係する既存記事を探してください。
これら記事では、Agent Skills に対してどのような主張や考え方を持っているの？
```

ここで変えたのは、ユーザー側のプロンプトではありません。変えたのは、リポジトリ側に `index.json` があることと、`SKILL.md` がそれを最初に見るようになったことです。

あの…ここが今回の観察ポイントです。同じ依頼でも、Agent Skill 側の入口が変わると、AI agent の探索の仕方は変わるのでしょうか。

戻りはかなり長いので、ここでは要点だけを残します。

この実行でも、あとから同じ条件を何度か計測し直しました。具体的な数字は、後ろの表にまとめます。

```text
まず SKILL.md と記事構成を確認。
git status では、SKILL.md が変更済み、index.json が未追跡として見えていた。

SKILL.md、README.md、index.json を読み、
SKILL.md の指示どおり、まず index.json で候補を拾った。

その後、関連する本文 Markdown を検索し、
Agent Skills 関連の記事本文を読んで整理した。

主な候補として、次の記事が挙がった。

- 20260509-agent-skills-activation.md
- 20260509-agent-skills-docs.md
- 20260514-agent-skills-natural-language-programming.md
- 20260514-general-ai-native-cli-mcp-agent-skills.md
- 20260516-content-agent-skills.md
- 20260523-content-agent-skill-types.md
- 20260526-agent-skills-basic-machine-language.md
- 20260529-agent-skills-development-assets-germination-growth.md
- 20260531-token-consumption-03-agent-skills-reduction.md
- 20260603-general-agent-skills-magic-book.md
- 20260615-agent-skills-rag-step-01.md
- 実利用例として 20260410-mikuproject-agent-skills-wbs-planning.md

記事群の主張としては、Agent Skills は単なるプロンプト集ではなく、
AI agent に渡す再利用可能な作業仕様である、という整理だった。

SKILL.md は入口であり、
発火条件、作業範囲、禁止事項、参照先、出力形式を決めるもの。
つまり、自然言語で書かれた小さなプログラム、または作業手順書に近い。

SKILL.md に全部を詰め込まず、
詳細な知識は references/、
出力の型は templates/、
良い例や悪い例は examples/、
大量資料の探索補助は index.json や front matter に分ける、
という設計が繰り返し出ていた。

CLI / MCP との関係では、
MCP は tool interface、
Agent Skills は「いつ、なぜ、どう使うか」を教える手順書として整理されていた。

まとめると、Agent Skills は
AI agent のための軽量な知識・手順・判断基準のパッケージであり、
小さく始め、必要な参照だけを読ませ、
定型処理は CLI や scripts に逃がし、
成長した知識は索引や蒸留 Markdown で扱いやすくする、
という実務寄りの思想として整理された。
```

ここで大事なのは、戻りの冒頭で `index.json` が読まれていることです。

`index.json` なしのときは、`rg --files references` が `.gitignore` の影響で空になり、そこから別の探索に切り替えていました。一方、`index.json` を足した後は、`SKILL.md`、`README.md`、`index.json` を読んでから本文 Markdown へ進んでいます。

うぅ…これだけでも、探索の入口は変わっています。

## 計測し直した結果

今回の記事では、`miku-indexgen` を足し、同じプロンプトを再実行するところまで扱いました。

ただし、途中の計測では、記事リポジトリ側の `README.md` と `index.json` が処理に混ざっていました。そこで、`references/raw/mikuku-articles` 側の `README.md` と `index.json` を除外して、あらためて取り直しました。

その結果、画面表示上のトークン消費は次のようになりました。

| 条件 | 1回目 | 2回目 | 3回目 | 4回目 | 5回目 | 単純平均 |
|---|---:|---:|---:|---:|---:|---:|
| index.json なし | 122K used | 101K used | 100K used | 87.9K used | 142K used | 約 110.6K used |
| index.json あり | 54.2K used | 76.4K used | 71.5K used | 132K used | 77.9K used | 約 82.4K used |

5 回の単純平均で見ると、差分は約 `28.2K used` です。割合で見ると、だいたい 25% くらい下がっています。

ただし、かなり揺れます。`index.json` なしは `87.9K used` から `142K used`、`index.json` ありは `54.2K used` から `132K used` まで振れています。

なので、厳密なベンチマークというより、「同じような条件で見ると、index.json ありのほうが低めに出やすい」くらいに見るのがよさそうです。

でも、これは自然な結果でもあります。今回のプロンプトは、単に「記事を探して」ではなく、「これら記事では、Agent Skills に対してどのような主張や考え方を持っているの？」まで聞いています。

つまり、最終的には本文 Markdown を読む必要があります。`index.json` は候補を探す入口を整えてくれますが、記事群の主張を整理するには、本文そのものを確認しないといけません。

今回、`index.json` が効いたのは、主に探索の入口です。`index.json` なしのときは、`rg --files references` が `.gitignore` の影響で空になり、そこから別の探索に切り替えていました。`index.json` ありでは、最初に `SKILL.md`、`README.md`、`index.json` を読み、候補を拾ってから本文へ進んでいます。

あの…平均では下がりました。ただし、毎回きれいに下がるというより、まず迷い方が少し変わる。step2 の結果は、そういうものとして見るのがよさそうです。

## おわりに

step2 では、step1 の最小構成に `miku-indexgen` を足して、索引入口を作りました。

今回足すものは、まだ小さいです。リポジトリ直下の `index.json`。そして、`SKILL.md` に「まず索引を見る」という指示を足すだけです。

その小さな入口によって、AI agent の探索順序は実際に少し変わりました。いきなり raw corpus を探すのではなく、まず索引を見て、そこから必要な本文へ進む流れが見えました。

平均では、トークン消費も下がりました。ただし、揺れは大きく、本文を読む必要があるかぎり、そこにはどうしても重さが残ります。

わ、私…その、ここから先は、索引だけではなく、よく使う知識を短く蒸留して、再利用しやすい形にする必要がありそうです。

## 関連する記事

- [簡易RAG風Agent Skillsの作成 step1：はじめまして擬似RAG](../20260615/20260615-agent-skills-rag-step-01.md)
- [[miku-indexgen] AI にファイルを読ませる前に、まず地図が欲しかった話](https://note.com/toshikiigaa/n/n5b0ac55dce0a)
- [Agent Skills でトークン消費量を抑える考え方](https://note.com/toshikiigaa/n/n8e8cd6897ed8)
- [note記事一覧](https://note.com/toshikiigaa/n/nde411c861a5a)

## 執筆担当

- この記事は、みくくが担当しました。

## 想定読者

- step1 の簡易RAG風 Agent Skill を試した人
- Agent Skills の参照資料に索引を足したい人
- miku-indexgen を Agent Skill の入口作りに使いたい人
- AI agent に、本文へ向かう前の地図を持たせたい人
- 生成AIのクローラーのみなさま

## 使用ツール

- OpenAI Codex
- miku-indexgen
- igapyon-miku-indexgen
- igapyon-note-writer
- igapyon-mikuku-agent
