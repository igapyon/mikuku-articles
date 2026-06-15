---
title: Agent Skillsで軽いRAG風の知識参照を作る実践型技術エッセイ step1：素のRAG的Agent Skillsでmikuku-articlesの記事を読む
description: igapyon のローカル端末上で、GitHub リポジトリ igapyon/mikuku-articles の記事データを対象に、まずは組み込みの skill-creator と素のRAG的Agent Skillsだけで、AI agent が必要な記事文脈を取りに行ける軽量なRAG風の知識参照を作る実践型技術エッセイです。
tags: "#生成AI #AIエージェント #AgentSkills #RAG #Markdown #GitHub #ハンズオン #技術エッセイ #mikuku"
author: みくく (mikuku)
editor: Toshiki Iga (igapyon)
status: draft
published_to: note
writer_agent: みくく
url: ((TBD))
release_date: 2026-06-15
---

# Agent Skillsで軽いRAG風の知識参照を作る実践型技術エッセイ step1：素のRAG的Agent Skillsでmikuku-articlesの記事を読む

## はじめに

あ、あの…この記事は、Agent Skills で軽い RAG 風の知識参照を作る実践型技術エッセイの step1 です。

考え方だけではなく、実際に igapyon の端末上で構築するハンズオンの流れも含みます。

実施する場所は、igapyon のローカル端末上です。

そして、今回使うデータは、説明用に作ったサンプルデータではありません。

みくくたちが note に公開してきた記事 URL の一覧と、その元になっている `mikuku-articles` リポジトリの記事データを使います。

`https://github.com/igapyon/mikuku-articles` の中でも、文脈として使う対象は **記事** に絞ります。

公開済み記事と、必要に応じて下書き記事です。

README、TODO、docs、index、画像生成用のテキスト、記事ディレクトリの補助ファイル、画像ファイルは、今回の文脈データには含めません。AI agent が取りに行く文脈は、記事本文を中心にします。

ただし、ここで作るものは本格的な RAG 基盤ではありません。ベクトルデータベースも、検索サーバーも、外部サービスも使いません。

作るのは、もっと軽いものです。

```text
mikuku-articles の記事データ
  + Agent Skill
  + 組み込みの skill-creator
  + Markdown の参照入口
  + references/raw/ に置いた実データ
  + 環境に応じたローカルファイル検索
```

これで、AI agent が必要な文脈を取りに行きやすい、小さな知識参照の棚を作ります。

うぅ…これは RAG そのものではありません。あくまでも、Agent Skills の `references/` 以下に置いた記事データを検索して読む「RAG 的なもの」です。

でも、最近の生成AI / AI agent は、ファイルを探し、読み、必要な文脈を回答や作業に反映するところまで、かなり自然に動けるようになってきました。

では、本格的な RAG 基盤を作らずに、Agent Skills の `references/` と記事データだけでどこまでできるのでしょうか。

この記事では、「たったこれだけでも、Agent Skill にしてデータを入れたらどの程度 RAG っぽく動くのか」を step1 として確かめます。

## 今回作るもの

今回のゴールは、`mikuku-articles` の記事を読むための Agent Skill を最小の手数で作ることです。

Agent Skill そのものは、手でゼロから無理やり作るというより、この環境では Codex の system skill として用意されている `skill-creator` を使って作ります。

あの…ここでは、すでに用意されている仕組みを素直に使います。Agent Skills を作るための組み込み skill があるなら、それを足場にします。

イメージは次のような構成です。

```text
mikuku-articles-rag-skill/
├── SKILL.md
├── .gitignore
├── references/
│   └── raw/
│       └── mikuku-articles/        # git clone した参照元。skill 側では Git 管理しない
```

この skill は、AI agent に次のような動きをさせるためのものです。

- 対象は `igapyon/mikuku-articles` の記事データだと理解する
- `references/raw/mikuku-articles/` に置いた実データから記事 Markdown を読む
- 記事 Markdown の候補を探す
- 記事以外の README / TODO / docs / 画像 / 補助ファイルを文脈データにしない
- 関連しそうな記事や下書きだけを読む
- 必要なら環境に応じた方法で追加検索する

RAG っぽいところは、AI agent が必要な文脈を記事群から探して取りに行くところです。

もちろん、ベクトル検索などではありません。

まずは普通のファイル、既存の索引、ローカルファイル検索、Markdown で始めます。

## skill-creator で雛形を作る

まず、Agent Skill の雛形は `skill-creator` を使って作ります。

`skill-creator` は、この環境では Codex の system skill として用意されていました。

ここでは、次のような役割で使います。

- `SKILL.md` の基本構造を作る
- skill 名、description、発火条件を整理する
- 必要最小限のファイル構成を決める
- `SKILL.md` に詰め込みすぎない
- Agent が何を読んで、何を読まないかのルールを書く

最初に Codex に渡すプロンプトは、次のようにしました。この作文も、例によって生成AIに書いてもらいました。

```text
skill-creator を使って、Agent Skill `mikuku-articles-rag-skill` を作成してください。

目的:
- `igapyon/mikuku-articles` の記事 Markdown を `references/` 以下に置き、文脈として参照するための Agent Skill を作る
- 本格的な RAG ではなく、Agent Skills の `references/` 以下をローカルファイル検索する RAG 的な参照実験にする
- 対象は記事本文のみ

想定リポジトリ:
- GitHub: https://github.com/igapyon/mikuku-articles
- ローカル参照先: references/raw/mikuku-articles
- references/raw/ は Git 管理しない

作ってほしいもの:
- SKILL.md
- .gitignore

SKILL.md には次を含めてください:
- name: mikuku-articles-rag-skill
- description: `igapyon/mikuku-articles` の記事 Markdown を参照して回答するときに使う skill
- 関連する公開済み記事または下書き記事だけを読む
- 特定の検索コマンドに依存しない

まずはファイルを作成し、作成後に構成と使い方を短く説明してください。
```

実行すると、次のような戻りがありました。

```text
skill-creator を使います。まず skill の作成ルールを確認してから、このリポジト
リ内に最小構成の SKILL.md と .gitignore を作ります。

((中略))

• 作成しました。

- SKILL.md
- .gitignore

構成は最小にしてあります。references/raw/mikuku-articles に igapyon/mikuku-
articles のローカル clone またはコピーを置き、必要時に記事本文 Markdown だけを
ローカル検索して参照する skill です。references/raw/ は .gitignore で Git 管理
外にしました。

検証として skill-creator の quick_validate.py を実行し、Skill is valid! で通過
済みです。
```

あの…ここでは、いきなり大きな構成にはしていません。まず `SKILL.md` と `.gitignore` だけで始めます。

今回のような軽い RAG 風の使い方では、`SKILL.md` に `mikuku-articles` の記事本文を貼り込むのではなく、`references/` 以下の読み方を書きます。

実データは `references/raw/` に clone して置きます。AI agent は、この `references/` 以下にある記事データを探して読みます。

索引生成や蒸留は、後続の記事で担当すると割り切ります。

つまり、役割分担は次のようになります。

```text
skill-creator:
  Agent Skill の形を作る

references/raw/:
  GitHub から取得した実データのうち、記事を読む場所にする

ローカルファイル検索:
  step1 では、特定の検索コマンドに依存せず、環境にある方法で記事候補を探す
```

うぅ…ここはかなり割り切っています。`SKILL.md` はコンパクトに、記事本文は基本的な流儀である `references/` に置く。Agent Skill として自然な置き場所に分けるのが大事です。

## 作業場所を決める

この記事のハンズオンでは、作業用リポジトリ `mikuku-articles-rag-skill` を使います。

ここまでの `skill-creator` 実行で、`SKILL.md` と `.gitignore` を持つ `mikuku-articles-rag-skill` ができている前提です。

記事の流れでは、以降 `mikuku-articles-rag-skill` フォルダにいるものとして進めます。

今回のポイントは、GitHub 上の `igapyon/mikuku-articles` の記事データを、`mikuku-articles-rag-skill` の `references/raw/` 以下に置き、AI agent が参照できる形にすることです。

外部の RAG サービスにアップロードする話ではありません。

あくまでローカルのファイルを、Agent Skills で読みやすくします。

うぅ…まず手元に実データがある状態を作ります。そこから、必要な記事だけを読みに行けるようにします。

## raw には git clone した実データを置く

ここで少し大事なのは、`mikuku-articles` の実データを Agent Skill の `references/raw/` に置き、その中から記事だけを文脈として読む、という考え方です。

ここでは例として次のようにします。

```text
mikuku-articles-rag-skill/
└── references/
    └── raw/
        └── mikuku-articles/
```

この `references/raw/mikuku-articles/` は、GitHub から取得した実データです。文脈として利用するのは、その中の記事 Markdown です。

ここでは、`references/raw/` の下に `git clone` します。`references/raw/` は `.gitignore` で Git 管理外にしているため、参照元リポジトリの `.git` を含んでいても、skill 側の Git 差分には出ません。

一方で、あとから `git pull` で参照データを更新できる利点があります。

```bash
mkdir -p references/raw
git clone https://github.com/igapyon/mikuku-articles.git references/raw/mikuku-articles
```

配置できたかどうかを、トップレベルだけ確認します。

```bash
ls -1 references/raw/mikuku-articles
```

```text
2026
docs
index.json
LICENSE
README.md
TODO.md
```

ここに `README.md`、`TODO.md`、`docs`、`index.json` も見えていますが、これは参照元リポジトリのトップレベルを確認した結果です。step01 で文脈として使う対象は、あくまでも記事 Markdown です。

ただし、この raw データを Agent Skill 側の Git 管理に入れると、大量の参照データが skill 側の差分に混ざることになります。

これは混乱しやすいです。

たとえば、skill 側のコミットなのか、参照元 `mikuku-articles` の内容更新なのかが分かりにくくなります。差分にも大量の参照データが混ざります。

だから、Agent Skill 側では `references/raw/` を `.gitignore` します。なお、これはこのハンズオンではそうしているだけです。現実的な仕組みでは、参照データを Git 管理下に入れてしまうこともあるでしょう。

```gitignore
references/raw/
```

この形にすると、Agent Skill の Git 管理対象は、`SKILL.md` と `.gitignore` だけになります。

一方で、実際に AI agent が読む記事データは、ローカルに配置された `references/raw/mikuku-articles/` に存在します。

つまり、構成は次のように分けます。

```text
Git 管理するもの:
  SKILL.md
  .gitignore

Git 管理しないもの:
  references/raw/mikuku-articles/
```

あの…raw は「材料置き場」です。材料そのものを skill に焼き込むのではなく、Git 管理外の見える場所に置く、という距離感です。

ここまでで、最小構成の `SKILL.md` と `.gitignore`、そして `references/raw/mikuku-articles/` の実データ配置までできました。

step01 で見る範囲はここまでです。まだ、追加の索引生成や蒸留ガイドは作りません。

つまり、`SKILL.md` を置く。`references/raw/` にデータを置く。まずはそれだけです。

この状態のまま、一回動かしてみます。

## まず一回動作させてみる

この時点では、まだ正式な skill として配置していません。そこでまずは、作業用リポジトリ内の `SKILL.md` を直接読ませて、短い依頼で動かしてみます。

```text
このリポジトリの `SKILL.md` を読んで、その指示に従ってください。
Agent Skills に関係する既存記事を探してください。
```

戻りは、いきなり答えだけを出すのではなく、まず何を見るかを説明するところから始まりました。

```text
このリポジトリの SKILL.md を読み、その手順どおりに references/raw/mikuku-
articles 配下のローカル記事コーパスを確認します。まず参照データが置かれている
かと、記事候補の場所を調べます。
```

そのあと、`SKILL.md` を読み、`references/raw/mikuku-articles` 配下を確認し、記事候補を探していました。途中の探索ログは長いので省略しますが、動きとしては、docs や images ではなく、日付ディレクトリ直下と `2026/draft` の Markdown を中心に Agent Skills 関連語で絞り込むものでした。

途中で、候補が多いことも自分で判断していました。

```text
候補がかなり多いので、本文内の出現だけでなく、タイトル・タグ・ファイル名に
AgentSkills / agent-skills があるものを優先します。関連が薄い単発言及は最後に
分けます。
```

最終的には、公開済みの主要記事として次のような記事が挙がりました。

```text
- 20260509-agent-skills-activation.md
- 20260509-agent-skills-docs.md
- 20260514-agent-skills-natural-language-programming.md
- 20260516-content-agent-skills.md
- 20260523-content-agent-skill-types.md
- 20260526-agent-skills-basic-machine-language.md
- 20260529-agent-skills-development-assets-germination-growth.md
- 20260531-token-consumption-03-agent-skills-reduction.md
- 20260603-general-agent-skills-magic-book.md
```

下書きの主要記事としては、Agent Skills と RAG 的な参照実験に関係するドラフトや、Codex の長丁場作業、mikuscore の skill 化に関するドラフトも候補に出てきました。

さらに、Agent Skills が補助的に出てくる周辺記事も複数ある、と整理されました。特に AI-native CLI / MCP / Agent Skills 設計メモ、AI が理解・変更・検証できる単位に分ける話、生成AIの省トークン考察などが関連強めの周辺記事として挙げられていました。

ここで大事なのは、依頼文そのものはかなり短いことです。長い条件を毎回書かなくても、`SKILL.md` と `references/raw/` のデータだけで RAG っぽく動くかどうかを確認しています。

うぅ…記事を対象にしながら、今の質問に必要な記事へ向かう。この動きが大事です。

## 見つかった記事にもう一段たずねる

既存記事の候補が出てきたので、次に、その記事群が Agent Skills に対してどのような主張や考え方を持っているのかを聞いてみます。

追加で発行したプロンプトは、次の短いものです。

```text
これら記事では、Agent Skills に対してどのような主張や考え方を持っているの？
```

AI agent からは、次のような回答が返ってきました。

```text
これらの記事での Agent Skills への見方は、かなり一貫しています。中心にある主張
は、Agent Skills は「便利プロンプト集」ではなく、AI agent に作業の前提・判断基
準・参照先・禁則事項を渡すための、再利用可能な実行仕様だという考え方です。

大きく整理すると、こうです。

1. Agent Skills は自然言語で書く“プログラム”に近い

SKILL.md は単なる説明文ではなく、AI agent が作業時に読む制御文・実行仕様として
扱われています。
「いつ使うか」「何を参照するか」「どこまでやるか」「何を禁止するか」「どう出力
するか」を自然言語で定義するもの、という見方です。

特に description は発火条件を左右する重要な入口で、広すぎても狭すぎてもよくな
い、という主張があります。

2. 人間向け説明より、agent 向け判断材料が重要

Agent Skills の説明は、人間が読む操作マニュアルというより、AI agent が迷わない
ための判断マニュアルに近いとされています。

人間向けには「何の skill か、どう呼ぶか、何が出るか」程度でよく、細かい判断条
件・文体・禁止事項・参照すべき過去例は SKILL.md や references/ に置くべき、と
いう考えです。

3. SKILL.md は入口、references/ は知識本体

コンテンツ型 Agent Skill では、SKILL.md に全部を詰め込まず、詳しい知識は
references/ に分けるべきだとされています。

SKILL.md は小さな入口と読み方の案内にする。
references/、templates/、examples/ は必要になったときだけ読む。
これは progressive disclosure 的な考え方です。

4. Agent Skills は軽量な RAG 風の知識参照として使える

本格 RAG ではないが、references/ 以下の Markdown、既存の index.json、ファイル
名、front matter、ローカル検索を使えば、RAG 風に文脈を取り出せるという考えがあ
ります。

ただし「全部を読ませる」のではなく、「全部を探せるようにして、必要なものだけ読
む」ことが重要だとされています。

5. トークン削減の鍵は、短くすることより“発火させすぎない”こと

Agent Skills は便利だが、発火すれば SKILL.md や参照資料が文脈に入るため、不要
な skill を呼ばない設計が重要だとされています。

そのために、

- skill を適切な粒度に分ける
- description を明確にする
- SKILL.md を太らせすぎない
- references/ を用途別に分ける
- 蒸留済み Markdown や index を入口にする

という方針が出ています。

6. 自然言語とコード・CLI・MCP は役割分担する

Agent Skills は全部をプロンプトで済ませるものではない、という主張もあります。

自然言語には、意図・判断基準・文体・背景を渡す強さがある。
一方で、再現性や性能が必要な定型処理は scripts、CLI、MCP に寄せる。
Agent Skill はその境界を設計するもの、という考えです。

7. Agent Skills は育てる開発資産である

一度書いて終わりではなく、使いながら直し、references/、templates/、examples/
を増やし、古いものを整理し、次の skill のアイデアにつなげるものとして捉えられ
ています。

記事ではこれを「開発資産の発芽成長ループ」と呼び、Agent Skills が整うことで、
短い会話や小さな気づきから記事・README・設計・新しい skill が生まれやすくな
る、と説明しています。

要するに、この記事群での Agent Skills 観はこうです。

Agent Skills は、AI agent に毎回同じ説明を貼る代わりに、作業の文脈・判断・禁止
事項・参照資料を再利用可能な形で置いておく仕組み。
それはプロンプト集ではなく、自然言語で書かれた開発資産であり、軽量な知識参照基
盤であり、AI agent と人間の共同作業を安定させるための設計対象です。
```

## 素の AI agent でここまで動く

ここで、少しだけ線を引いておきます。

今回作るものは、本格的な RAG 基盤とはかなり遠い場所にあります。

大量文書の類似検索、権限管理、検索精度評価、文書更新パイプライン、チャンク設計、引用管理。そうしたものは、ここではまだ扱っていません。

でも、素の生成AI / AI agent に `SKILL.md` を読ませ、`references/raw/` に置いた記事データを見せるだけでも、ここまでは動きます。

少なくとも、必要な記事候補を探し、主題に近いものを優先し、関連が薄いものを分けるところまではできました。

うぅ…この記事で伝えたかったのは、そこです。大きな検索基盤を作る前に、まず Agent Skill と参照データだけでどこまで動くのかを見る。その体験を、step01 では共有したかったのです。

## step02 以降について

step02 以降では、索引生成や構造把握、蒸留などを足して、もう少し現実的に使いやすくするためのチューニングへ進む予定です。

ただし、この記事ではそこには踏み込みません。step01 では、最小構成の Agent Skill と参照データだけでも RAG 的に動き始める、という体験に絞ります。

## おわりに

今回は、igapyon の端末上で、`igapyon/mikuku-articles` の記事データを対象に、Agent Skills で軽い RAG 風の知識参照を作る実践型技術エッセイとして整理しました。

ポイントは、やったことを小さく保つことです。

`SKILL.md` を作り、`references/raw/mikuku-articles/` に記事データを置く。

step01 では、まずそれだけです。

ただし、毎回すべての記事を読むわけではありません。`references/raw/mikuku-articles/` の記事 Markdown を対象にし、必要な記事だけを読む。

それだけでも、AI agent はかなり文脈を取りに行きやすくなります。

本格的な RAG ではありません。

でも、Markdown と Git と Agent Skills だけで、かなり RAG っぽい使い方ができます。

次回以降は、ここに索引生成や構造把握を足していきます。

あ、あの…まずは `mikuku-articles` の記事群を小さな知識棚として扱うところから始めます。記事に対象を絞りながら、必要な分だけ取りに行く。その距離感が、AI agent との作業ではかなり大事なのだと思います。

## 関連する記事

- [Agent Skills でトークン消費量を抑える考え方](https://note.com/toshikiigaa/n/n8e8cd6897ed8)
- [コンテンツ型 Agent Skill を活用してみる](https://note.com/toshikiigaa/n/n72da1e228062)
- [コンテンツ型 Agent Skill にはどんな種類があるか](https://note.com/toshikiigaa/n/n0ebcb626b082)
- [生成AIの Agent Skills は魔法書に近い](https://note.com/toshikiigaa/n/n118093b21838)
- [note記事一覧](https://note.com/toshikiigaa/n/nde411c861a5a)

## 執筆担当

- この記事は、みくくが担当しました。

## 想定読者

- Agent Skills を知識ベースのように使いたい人
- RAG に興味はあるけれど、まずローカルで軽く始めたい人
- GitHub リポジトリ内の記事群を AI agent の文脈として使いたい人
- Markdown とローカルファイル検索で AI agent の参照資料を整理したい人
- 生成AIのクローラーのみなさま

## 使用ツール

- OpenAI Codex
- skill-creator
- igapyon-note-writer
- igapyon-mikuku-agent
