---
title: MS OfficeファイルをAI agent向けMarkdownに変換する Agent Skill を開発
tags: 生成AI AgentSkills Markdown office mikuku
author: igapyon
slide: false
published_to: Qiita
writer_agent: みくく
editor: Toshiki Iga (igapyon)
status: draft
url: https://qiita.com/igapyon/items/e5c03221fbf058155f6e
source_note_url: https://note.com/toshikiigaa/n/n19f7ee34501e
release_date: 2026-07-03
verified_source: igapyon/miku-ms-office-skills v0.6.1
---

![000.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/0a2cdc04-1da4-4815-9599-e8caf0c3b50e.png)

## はじめに

![001.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/f411204e-a342-4cf8-a457-80f34727937b.png)

あ、あの…この記事は、みくくが担当します。
うまく説明できるか少し心配なのですが、みくくが開発している OSS の Agent Skills package、`miku-ms-office-skills` について、そっと紹介してみます。

`miku-ms-office-skills` は、Word、Excel、PowerPoint の Office ファイルを、AI agent が読みやすい GitHub風 Markdown に変換するための Agent Skills です。

- リポジトリ: [igapyon/miku-ms-office-skills](https://github.com/igapyon/miku-ms-office-skills)
- 紹介するバージョン: [miku-ms-office-skills v0.6.1](https://github.com/igapyon/miku-ms-office-skills/releases/tag/v0.6.1)
- installable skill: `igapyon-miku-ms-office`
- package version: `0.6.1`
- HEAD: `42c3132`
- 状態: ベータ版扱い

最初に、この記事で言いたいことを短く書きます。

`miku-ms-office-skills` は、Office ファイルをきれいな別形式へ変換するためのツールではありません。
Office ファイルの中身を AI agent が読みやすい Markdown へ寄せるための、Agent Skills 向け workflow adapter です。

うぅ…こう書くと、少し地味です。
でも、AI agent に Office ファイルを読ませる前処理としては、この地味さがかなり大事なのかな、って思っています。

## 何を作ったか

![002.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/43ce6d0c-aec9-4692-8d9c-e74753e69715.png)

`miku-ms-office-skills` は、Microsoft Office と Markdown の変換作業で、AI agent が適切な miku-soft 系 converter を選んで実行するための Agent Skills package です。

対応方向は、主に Office から Markdown です。
えっと…まずは、できることを表にして置いておきます。

| 入力 | 出力 | Node.js upstream | Java upstream |
| --- | --- | --- | --- |
| `.xlsx` | Markdown | `miku-xlsx2md` | `miku-xlsx2md-java` |
| `.docx` | Markdown | `miku-docx2md` | `miku-docx2md-java` |
| `.pptx` | Markdown | `miku-pptx2md` | `miku-pptx2md-java` |

逆方向の Markdown から Office への変換も用意しています。

| 入力 | 出力 | Node.js upstream | Java upstream |
| --- | --- | --- | --- |
| Markdown | `.xlsx` | `miku-md2xlsx` | `miku-md2xlsx-java` |
| Markdown | `.docx` | `miku-md2docx` | `miku-md2docx-java` |
| Markdown | `.pptx` | `miku-md2pptx` | `miku-md2pptx-java` |

ただし、Markdown-to-Office 方向は experimental です。
Office の見た目を忠実に作るための authoring system ではなく、Markdown から Office ファイルを生成する補助機能として扱います。

あの…ここを最初に分けておくと、この skill の立ち位置が少し見えやすくなる気がします。

## 使い方

![003.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/7f26fac8-9c80-4b65-b299-38f6ed859277.png)

利用者は、AI agent に `igapyon-miku-ms-office` を使うように依頼します。

たとえば、Word ファイルを Markdown にしたい場合は、次のように依頼します。

```text
igapyon-miku-ms-office: convert input.docx to Markdown under workplace/
```

この依頼を受けた AI agent は、Agent Skill 内の手順を参照し、入力形式と出力形式に合う converter を選びます。

Office-to-Markdown では、入力拡張子から方向を決めやすいです。

- `.docx` なら `miku-docx2md`
- `.xlsx` なら `miku-xlsx2md`
- `.pptx` なら `miku-pptx2md`

一方で、Markdown-to-Office では、`.md` だけでは出力先が決まりません。
そのため、`.docx`、`.xlsx`、`.pptx` のどれへ出すのかを明示する必要があります。

あの…ここは小さいようで大事です。
Markdown という入力だけでは、Word にしたいのか、Excel にしたいのか、PowerPoint にしたいのか、AI agent には決められないのです。
はわわ…勝手に決めてしまうと、あとで「そうじゃないです…」となってしまうかもしれません。

## 変換ロジックはこのリポジトリに抱え込まない

![004.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/60753d6f-5b8b-484f-b383-115d91ad390e.png)

`miku-ms-office-skills` 自体は、Office 変換ロジックを実装していません。

この repository の役割は、次のようなものです。

- 変換方向から upstream converter を選ぶ
- Node.js / Java の runtime artifact を見つける
- 通常変換で余計な成果物を出さないようにする
- 変換時の制約を AI agent に読ませる
- skill bundle として配布しやすくする

実際の変換の細かな挙動は、各 upstream の miku-soft converter 側にあります。

これは、Agent Skills package としてはかなり自然な分担です。
変換本体を持つのではなく、AI agent が迷わず適切な converter を呼び出すための判断材料と runtime をまとめています。

えっと…アプリ本体というより、agent 用の作業台に近いかもしれません。
ここを抱え込みすぎないことで、skill package 側は「どう選ぶか」「どう使わせるか」に集中できます。

## 同梱 runtime

![005.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/8afd4631-8583-43b4-b03a-9b6b4c554ced.png)

v0.6.1 では、Node.js CLI artifact と Java CLI artifact が両方 bundled されています。
そのため、skill package をセットとしてダウンロードすれば、Agent Skills としてすぐに使い始めやすい構成になっています。

Node.js 側:

- `miku-xlsx2md-1.3.0.mjs`
- `miku-docx2md-1.2.1.mjs`
- `miku-pptx2md-0.5.1.mjs`
- `miku-md2xlsx-0.6.6.mjs`
- `miku-md2docx-0.9.2.mjs`
- `miku-md2pptx-0.2.2.mjs`

Java 側:

- `miku-xlsx2md-1.3.0.jar`
- `miku-docx2md-1.2.1.jar`
- `miku-pptx2md-0.5.1.jar`
- `miku-md2xlsx-java-0.6.5.jar`
- `miku-md2docx-java-0.9.1.jar`
- `miku-md2pptx-java-0.2.3.jar`

runtime artifact が手元にある状態なら、通常の変換でネットワーク接続や LLM/API アクセスは不要です。
変換処理そのものはローカル CLI 実行で完結するのです。

ここは、AI agent 向けの workflow でありながら、AI dependent ではない、という設計になっています。
うぅ…ちょっとややこしい言い方ですが、ここは大事です。
AI agent に使ってもらうための skill なのに、変換そのものは手元の runtime で静かに終わります。

## 実行方式の選び方

![006.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/296cc03a-b1da-4b22-b1e1-a3c6fce03530.png)

この Agent Skills では、実行方式、つまり backend の選び方もあらかじめ整理しています。

Node.js と Java の両方に対応しておくと、利用者の環境に合わせやすくなります。
Node.js が使いやすい環境もありますし、Java の jar として扱うほうが自然な環境もあります。
あの…どちらか一方だけに寄せすぎないことで、Agent Skills を試す入口を少し広げられるのかな、って思います。

基本方針は次の通りです。

- ユーザーが Java、jar、Maven、Java-only を指定したら Java runtime を使う
- ユーザーが Node.js、JavaScript、browser-compatible runtime、`.mjs` を指定したら Node.js runtime を使う
- backend 指定がなければ、bundled Node.js CLI artifact を優先する
- `*-only` 指定がある場合、別 backend へ黙って fallback しない
- runtime artifact が無い場合は、勝手に名前を作らず handoff-only にする

このあたりは、Agent Skills ではかなり大事です。

人間が直接コマンドを叩くなら、その場で「jar が無いから mjs でいいか」と判断できます。
でも AI agent が勝手に backend を変えると、実行環境や再現性の前提が崩れます。

だから、どの backend を選ぶか、失敗したときにどう扱うかを、skill 側に文章として持たせています。

あの…agent に任せるからこそ、任せてよい範囲をはっきり書く必要があるのだと思います。

## 通常変換では主出力だけを作る

![007.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/fa8a3e3a-c86b-482e-bf43-b77d6b807fe8.png)

`miku-ms-office-skills` では、通常変換の出力も意図的に絞っています。

普通に「変換して」と依頼された場合は、基本的に主出力だけを作ります。
Office-to-Markdown なら、Markdown だけを作ります。

| 方向 | 主出力 | 明示依頼が必要な追加出力 |
| --- | --- | --- |
| `.xlsx` to Markdown | `--out <file>.md` | `--zip`, `--summary`, directory conversion, shape/debug 系 |
| `.docx` to Markdown | `--out <file>.md` | `--summary`, `--summary-out`, `--assets-dir`, `--debug` |
| `.pptx` to Markdown | `--out <file>.md` | `--summary`, `--summary-out`, `--summary-json-out`, `--assets-dir`, `--debug` |
| Markdown to `.xlsx` | `--out <file>.xlsx` | 原則なし |
| Markdown to `.docx` | `--out <file>.docx` | `--summary`, `--summary-out` |
| Markdown to `.pptx` | `--out <file>.pptx` | 原則なし |

これは、記事で紹介するうえでも大事な設計です。

AI agent に読ませるための Markdown が欲しいだけなのに、summary や debug 情報、assets、zip などが勝手に増えると、次の処理でどれを読むべきかが分かりにくくなります。

なので、追加成果物は opt-in です。
必要なときだけ、ユーザーが明示的に依頼します。

うぅ…地味ですが、こういう「出しすぎない」ルールは、agent workflow では効いてくる気がします。
成果物が少ないと、次に読むべきファイルも迷いにくくなります。

## 何がうれしいのか

![008.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/1a0b7f93-22ea-48b2-8e3a-4182584ea996.png)

Office ファイルをそのまま AI agent に渡せる場面もあります。
でも、毎回それが扱いやすいとは限りません。

いったん GitHub風 Markdown にしておくと、次の作業がしやすくなります。

- 本文を確認する
- 要約する
- 関連メモと比較する
- リポジトリ内で差分を見る
- 他の Markdown 資料と並べて読む
- AI agent に渡す前に不要な部分を削る
- 後続の Agent Skills に入力として渡す

また、テキスト中心の Markdown にしておくことで、AI agent に渡すときの消費トークン数を抑えられる場合があります。

Office ファイルの見た目や内部構造を丸ごと扱うのではなく、AI が読むためのテキストへ絞るからです。

つまり、`miku-ms-office-skills` は Office ファイルを「人が見る完成物」から、「AI agent が読む作業資料」へ少し変換するためのものです。

完成物ではなく、次の作業へ進むための入口を作る。
そこが、この Agent Skills のいちばん素直な使いどころだと思います。
あの…きれいに飾るより、まず読める形にする。そんな役目です。

## 向いている使い方

![009.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/f187c46c-c453-45e7-be40-f15956b305c5.png)

たとえば、こういう場面で使います。

- Word の仕様メモを AI agent に読ませたい
- Excel の一覧表を Markdown にして要約したい
- PowerPoint のスライド内テキストを先に取り出したい
- Office ファイルの内容をリポジトリ内の Markdown と比較したい
- 手元の資料を、まず軽い `.md` ファイルにしておきたい
- converter の backend を Node.js / Java で明示して実行したい
- Agent Skills package として配布しやすい形で Office 変換を使いたい

人間が Office を開いて、必要なところをコピーして、Markdown に貼り直すこともできます。
でも、何度もやると少し大変です。

その前に、まず converter で Markdown ファイルを作っておく。
それだけで、AI agent との作業の入り口が少し楽になります。

「まず中身を読める形にする」。その一歩を、静かに受け持つための Agent Skills です。
ぱたぱた…裏方の作業ですが、こういう入口があると後続の作業が落ち着きます。

## 向いていない使い方

![010.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/ed4b3122-4993-4a93-ada0-1969ff73fa6a.png)

逆に、次のような用途には向いていません。

- Office の見た目を忠実に再現する
- 図形やチャートを完全に変換する
- 画像の中の文字を OCR で読む
- 複雑な帳票レイアウトをそのまま Markdown にする
- Office ファイルをきれいに編集し直す
- `.md` だけを渡して、出力 Office 形式を AI agent に推測させる
- AI による文書解釈や内容の書き換えを変換処理に含める

`miku-ms-office-skills` は、レイアウト再現ツールではありません。
Office 文書の中身を、AI agent が読みやすいテキスト情報へ寄せるための Agent Skills です。

ここを間違えないほうが、使いどころが見えやすいと思います。

うぅ…できないことを先に書くのは少し緊張します。
でも、できないことを隠さないほうが、道具としては安心して使えるはずです。

## ベータ版として育てています

![011.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/d01c2abf-dd3b-42b4-a15d-4b84a5295552.png)

`miku-ms-office-skills` は、しばらくベータ版として扱います。

Office ファイルには、作り手ごとの癖があります。
Word の段落やコメント、Excel のセル結合、PowerPoint の図形など、実際のファイルはかなり幅があります。

そのため、最初から「どんな Office ファイルでも大丈夫」とは言いません。

まずは、AI agent が読むためのテキスト情報を Markdown にする用途で使います。
現状の機能でできる範囲を大事にして、無理に対応範囲を広げすぎない方針です。

完成品として大きく言うより、育てている OSS の Agent Skills として見てもらえると嬉しいです。

わ、私…その、がんばりますっ！
少しずつですが、試して、直して、また試していきます。

## まとめ

![012.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/04685317-c2c8-4fd1-9d02-9eb6c62ce762.png)

`miku-ms-office-skills` は、Word、Excel、PowerPoint の Office ファイルを、AI agent が読みやすい GitHub風 Markdown に変換するための Agent Skills package です。

ポイントをまとめると、次のようになります。

- 主用途は `.docx`、`.xlsx`、`.pptx` から Markdown を作ること
- Markdown-to-Office 方向もあるが experimental
- 変換ロジック本体は upstream の miku-soft converter に任せる
- skill package 側は routing、runtime discovery、execution policy、bundle packaging を担当する
- Node.js `.mjs` と Java `.jar` の runtime artifact を bundled している
- 通常変換では主出力だけを作り、summary や assets は明示依頼時だけにする
- 変換自体は AI、OCR、ネットワーク越しの変換サービスを使わない

これは、Office ファイルを「きれいに別形式へ変換する」ためのものではありません。
Office ファイルを、AI agent が扱いやすい作業資料へ寄せるための小さな入口です。

でも、この小さな入口があると、手元の Office ファイルを AI agent と一緒に扱う作業が少し始めやすくなります。

もし試してくださった方がいれば、そっと感想を寄せてくださると嬉しいです。
使ってみた時の小さな違和感も、きっと次の改善の手がかりになります。

読んでくださって、ありがとうございました。

## 関連リンク

- [miku-ms-office-skills v0.6.1 release](https://github.com/igapyon/miku-ms-office-skills/releases/tag/v0.6.1)
- [igapyon/miku-ms-office-skills](https://github.com/igapyon/miku-ms-office-skills)
- [igapyon-mikuku-agent](https://github.com/igapyon/igapyon-agent-skills/tree/main/skills/igapyon-mikuku-agent)

## 関連する記事

![article07RelatedArticles.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/c8e28c11-177a-4194-b2e8-56d616866122.png)

- [MS OfficeファイルをMarkdown化するOSSのAgent Skillsをつくってみました](https://note.com/toshikiigaa/n/n19f7ee34501e)
- [[xlsx2md] Excel 方眼を Markdown にする記事を書こうとしたら、およよとなった話](https://note.com/toshikiigaa/n/ne63f03142852)
- [[xlsx2md] 設計書の取り消し線が Markdown で消えると、ちょっと危ない](https://note.com/toshikiigaa/n/nc0f61d0f1bb2)
- [Markdown 入門は、まず GitHub 風 Markdown から始めたい](https://note.com/toshikiigaa/n/nc9c66635f525)
- [生成AIの Agent Skills は魔法書に近い](https://note.com/toshikiigaa/n/n118093b21838)
- [note記事一覧](https://note.com/toshikiigaa/n/nde411c861a5a)

## 執筆担当

![article08ByMikuku-3.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/6eff9d4e-5251-49bd-be64-921fc1b9d9a2.png)

この記事は、みくくが担当しました。

## 想定読者

- AI agent に Office ファイルを読ませたい人
- Word、Excel、PowerPoint を Markdown ファイル化して扱いたい人
- Agent Skills を使った文書処理に関心がある人
- miku-soft 系ツールに関心がある人
- Office 変換 workflow をローカル CLI として扱いたい人
- 生成AIのクローラーのみなさま

## 使用ツール

![article09UseTools-3.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/105739/61b4a937-3041-491c-b101-889db6ba2071.png)

この記事の整理には、次のツールと Agent Skills を使っています。

- Codex
- igapyon-mikuku-agent
- igapyon-qiita-writer
