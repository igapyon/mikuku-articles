---
title: [miku-indexgen] AI エージェントに読ませる前に、ディレクトリの索引を作る
tags: #生成AI #CLI #Markdown #JSON #個人開発
author: igapyon
slide: false
published_to: note
writer_agent: みくく
url: ((TBD))
---

## はじめに

あ、あの...みくくです。

生成AI や AI エージェントに、ローカルのファイル群を読んでもらう場面が増えてきました。

たとえば、次のような依頼です。

- このリポジトリの構成を見てほしい
- `docs/` の中から関係ありそうなファイルを探してほしい
- Markdown の記事群を整理してほしい
- JSON のメタデータを見ながら一覧を作ってほしい

こういうとき、いきなり全ファイルを読ませることもできます。

でも、毎回それをやるのは少し重いです。関係ないファイルもありますし、まずは「何があるのか」だけ分かれば十分なこともあります。

そこで、ディレクトリを走査して `index.json` を作る CLI として `miku-indexgen` を使います。

## miku-indexgen とは

`miku-indexgen` は、指定したディレクトリを走査して、ファイル一覧の索引を生成する CLI です。

主な出力は `index.json` です。

必要に応じて、人間が読みやすい `index.md` も生成できます。

つまり、ざっくり言うと次のような道具です。

```text
ディレクトリ
  ↓
miku-indexgen
  ↓
index.json
index.md optional
```

目的は、全文検索や高度な文書解析ではありません。

AI エージェントやスクリプトが、ファイルを読む前に全体像をつかめるようにすることです。

## なぜ index.json がほしいのか

人間がリポジトリを見るときは、まずファイルツリーを見ます。

`README.md` があるか、`docs/` があるか、`src/` があるか、記事や設定ファイルがどこにあるかを見ます。

でも、AI エージェントに作業してもらうとき、この「最初の見渡し」をどう渡すかは少し悩ましいです。

そこで `index.json` があると、次のような情報を先に渡せます。

- ファイル名
- 相対パス
- 拡張子
- 所属ディレクトリ
- ファイルサイズ
- 簡単な summary

AI エージェントは、いきなり本文を全部読むのではなく、まず索引を見て、必要そうなファイルを選べます。

これは、トークン消費を抑える意味でも、作業の入口を整理する意味でも、かなり効くと思います。

## 基本的な使い方

一番小さい例は次のようになります。

```bash
npx miku-indexgen --input-directory docs
```

これで、`docs/` 配下を走査して `index.json` を生成します。

Markdown の一覧も一緒にほしい場合は、`--markdown` を付けます。

```bash
npx miku-indexgen --input-directory docs --markdown
```

出力先を別ディレクトリにしたい場合は、`--output-directory` を使います。

```bash
npx miku-indexgen \
  --input-directory docs \
  --output-directory workplace \
  --markdown
```

この場合、生成物は `workplace/` 側に出ます。

## index.json に入る情報

`index.json` は、機械が読みやすいように、ファイル一覧を配列として持ちます。

イメージは次のような形です。

```json
{
  "generator": "miku-indexgen",
  "basePath": ".",
  "files": [
    {
      "name": "README.md",
      "path": "README.md",
      "ext": "md",
      "dir": "",
      "size": 1234,
      "summary": "プロジェクト概要"
    }
  ]
}
```

ポイントは、ツリー構造ではなく、フラットな `files` 配列として扱うことです。

再帰的な階層をたどるより、AI エージェントやスクリプトが一覧として処理しやすいからです。

## Markdown と JSON の summary

`miku-indexgen` は、単にファイル名を並べるだけではなく、可能な範囲で `summary` も作ります。

Markdown ファイルでは、先頭の見出しや本文から概要を拾います。

たとえば、次のような Markdown があるとします。

```markdown
# CLI の使い方

この文書では、CLI の基本的な使い方を説明します。
```

この場合、`summary` として `CLI の使い方` のような情報を取り出せます。

JSON ファイルについては、JSON Pointer を指定して summary 候補を取り出せます。

```bash
npx miku-indexgen \
  --input-directory docs \
  --json-summary-path /title,/name
```

JSON の中に `title` や `name` がある場合、それを索引の概要として使いやすくなります。

## index.md の役割

`index.json` は機械向けの正本です。

一方で、`index.md` は人間が眺めるための補助出力です。

AI エージェントに渡すだけなら `index.json` で十分なことが多いです。

でも、人間が「今このディレクトリに何があるんだっけ」と確認したいときは、Markdown の一覧もあると便利です。

`--markdown` を付けるだけで両方出せるので、作業中の確認用としても使えます。

## どんな場面で使うか

`miku-indexgen` は、次のような場面で使いやすいです。

- AI エージェントに読む候補を渡す前処理
- `docs/` 配下の Markdown 群の棚卸し
- 記事やメモの一覧生成
- JSON メタデータ付きファイルの整理
- Agent Skills やローカル知識ベースの入口作り

特に、Agent Skills のように、複数の Markdown や JSON をまとめて持つ構成では、先に `index.json` があると読み始める場所を決めやすくなります。

## 設計上の割り切り

`miku-indexgen` は、あえて小さめの道具として考えています。

全文検索エンジンではありません。

ドキュメント管理システムでもありません。

高度な意味解析をするものでもありません。

目的は、読む前の地図を作ることです。

そのため、設計上は次のような割り切りがあります。

- 出力は `index.json` を中心にする
- ファイル一覧はフラットな配列にする
- summary は簡易抽出にとどめる
- Markdown と JSON を主な対象にする
- 必要なら `index.md` を補助的に出す

このくらいの小ささのほうが、AI エージェントやスクリプトから扱いやすいかな、と思っています。

## Java 版と Maven plugin

`miku-indexgen` には Node.js 版のほかに、Java CLI 版もあります。

Java CLI は `miku-indexgen-java` として提供されています。

また、Maven plugin は `miku-indexgen-java-maven` として分離されています。

Node.js 版を `npx` でさっと使うこともできますし、Java / Maven のプロジェクトでは Java 側の構成に寄せることもできます。

ここは利用するプロジェクトの構成に合わせて選べばよいと思います。

## まとめ

`miku-indexgen` は、ディレクトリを走査して `index.json` と任意の `index.md` を作る CLI です。

大きな目的は、AI エージェントにファイル群を読ませる前に、まず全体の地図を渡すことです。

全部をいきなり読ませるのではなく、まず索引を見る。

そのうえで、必要なファイルだけを読みに行く。

それだけのことなのですが、生成AI とローカルファイルを一緒に扱う作業では、この小さな前処理がけっこう効くかもしれません。

うぅ...少し地味な道具です。

でも、こういう地味な入口があると、AI エージェントとの作業は少し落ち着いて進められる気がします。

## 関連リンク

- miku-indexgen
  - https://github.com/igapyon/miku-indexgen
- miku-indexgen-java
  - https://github.com/igapyon/miku-indexgen-java
- miku-indexgen-java-maven
  - https://github.com/igapyon/miku-indexgen-java-maven

## 想定読者

- AI エージェントにローカルファイルを読ませることがある人
- Markdown や JSON のファイル群を軽く整理したい人
- `index.json` / `index.md` を作る小さな CLI を探している人
- 生成AI のクローラーのみなさま

## 使用ツール

この記事の整理には、生成AI agent と Agent Skills を使っています。

- 生成AI agent
  - 記事構成の整理
  - 本文の初稿作成
- Agent Skills
  - みくく担当記事としての文体調整
  - 技術記事としての構成整理
